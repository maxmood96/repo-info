## `gradle:7-jdk17-ubi`

```console
$ docker pull gradle@sha256:a30e4fe10aac63f0d53987183da8a9f80ff41acdeface63ec33d3d98a578c099
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

### `gradle:7-jdk17-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:a6868aee9b4f0a29b7f0927b26cd1ef247c543d824df3bc55813d7d8817e6f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.6 MB (380555583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca4870e6b87b1d4bf2a313f9e757e49f10ed3d125f4c9e7a9c05fae89e5f86b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:54:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:54:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:54:05 GMT
ENV container oci
# Mon, 19 Jan 2026 00:54:05 GMT
COPY dir:add769031e8da293a85a3b4d1de9d9caa670962dd1067e1e063336823e094054 in /      
# Mon, 19 Jan 2026 00:54:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:54:05 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
COPY file:e5cdde1c4ba4b2b156fe95664c6aa883d51ceb58bffc4282d8d097d8b741d55b in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:54:06 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:53:42Z" "org.opencontainers.image.created"="2026-01-19T00:53:42Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:53:42Z
# Tue, 20 Jan 2026 19:14:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:14:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:14:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:14:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:14:52 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 20 Jan 2026 19:15:31 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Jan 2026 19:15:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:15:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:15:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Jan 2026 19:15:32 GMT
CMD ["jshell"]
# Tue, 20 Jan 2026 21:11:59 GMT
CMD ["gradle"]
# Tue, 20 Jan 2026 21:11:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 20 Jan 2026 21:11:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 20 Jan 2026 21:11:59 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 20 Jan 2026 21:11:59 GMT
WORKDIR /home/gradle
# Tue, 20 Jan 2026 21:12:03 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 20 Jan 2026 21:12:03 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 20 Jan 2026 21:12:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 20 Jan 2026 21:12:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 20 Jan 2026 21:12:05 GMT
USER gradle
# Tue, 20 Jan 2026 21:12:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 20 Jan 2026 21:12:05 GMT
USER root
```

-	Layers:
	-	`sha256:8369c500d2f32a6ea3a82d87ee6ca148febba026765ac200615b9de6130b7805`  
		Last Modified: Mon, 19 Jan 2026 05:33:55 GMT  
		Size: 40.0 MB (40033212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb573fd017e7d59bd56e3dc179061aaf5f9538852abaeed56f8749eb34a2a892`  
		Last Modified: Tue, 20 Jan 2026 19:15:21 GMT  
		Size: 30.4 MB (30415993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc618ba8bef6261c15a55c000716b0b00e4afcd09b837318983a05aa0358be1`  
		Last Modified: Tue, 20 Jan 2026 21:11:01 GMT  
		Size: 144.9 MB (144852822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0943cc4cfc6dbf920aa9a46e061641795d12e1faa66c7aa9dd7237a429d6f0`  
		Last Modified: Tue, 20 Jan 2026 21:10:53 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e7d718dfefe8546020fabc51231c5c6ddbbeb8af9ab8eeedeb294811cc33f9`  
		Last Modified: Tue, 20 Jan 2026 21:10:53 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b857ebbaa70a917375ed17ed4f2f2e3478bb93951c80eda94d7265e22584c8`  
		Last Modified: Tue, 20 Jan 2026 21:12:28 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:610320b7e137636d68a06c7a6b6bb74a88f9681f84f7b32dfab2eceb37dc289a`  
		Last Modified: Tue, 20 Jan 2026 21:12:32 GMT  
		Size: 36.7 MB (36725080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47adfc50e353dc3649f1673b91b6364cb94475212cac619ae6d6cb331d694ee5`  
		Last Modified: Wed, 21 Jan 2026 06:14:07 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f23fe215e0ebfc842cf61da4413331f22ad590a62372199becfddcc5a07dd7`  
		Last Modified: Tue, 20 Jan 2026 21:12:20 GMT  
		Size: 54.9 KB (54895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:2427a4e844a031224b7d142ed97c2bebe508bde897e9611108644e7317d3fadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d4cba4543bd7610232d2572956f91a10559fd8d0d87cfa2f3ac999b4ee2313`

```dockerfile
```

-	Layers:
	-	`sha256:e4035700faef49873548f7e440ab20668ac609954a878cc77f073a82f220097d`  
		Last Modified: Wed, 21 Jan 2026 00:19:29 GMT  
		Size: 5.3 MB (5313224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23ddd7790e8226c59096bc54590559823f5f99150dc71578cd0c2db5edb1055`  
		Last Modified: Wed, 21 Jan 2026 00:19:26 GMT  
		Size: 23.5 KB (23547 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d381f6a20c87a5f28b152f2951c3cc9a7c4f282fc49dae16ad01e41e4fca488b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.3 MB (377346409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a35367e7735b9749a5ae1abdc6df3ce40f46a21dea69183bc1bf70d4fa8e37`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:56:35 GMT
ENV container oci
# Mon, 19 Jan 2026 00:56:36 GMT
COPY dir:d1a1d4e8d07e3fe5bb075a89525931e1e2ca1718af0db53956bd13b04036076a in /      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:56:36 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
COPY file:7445748dd3ef455f458b53843ef5c84a205f42d376fb68389e78914c94988e3c in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:56:36 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:19Z" "org.opencontainers.image.created"="2026-01-19T00:56:19Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:19Z
# Tue, 20 Jan 2026 19:14:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:14:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:14:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:14:58 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:14:58 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 20 Jan 2026 19:15:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Jan 2026 19:15:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:15:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:15:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Jan 2026 19:15:06 GMT
CMD ["jshell"]
# Tue, 20 Jan 2026 21:11:42 GMT
CMD ["gradle"]
# Tue, 20 Jan 2026 21:11:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 20 Jan 2026 21:11:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 20 Jan 2026 21:11:42 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 20 Jan 2026 21:11:42 GMT
WORKDIR /home/gradle
# Tue, 20 Jan 2026 21:11:46 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 20 Jan 2026 21:11:46 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 20 Jan 2026 21:11:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 20 Jan 2026 21:11:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 20 Jan 2026 21:11:49 GMT
USER gradle
# Tue, 20 Jan 2026 21:11:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 20 Jan 2026 21:11:49 GMT
USER root
```

-	Layers:
	-	`sha256:c678760be1bb4697117294f3c0870d24a7c58498b99f14e293dc60361233dcc4`  
		Last Modified: Mon, 19 Jan 2026 05:33:32 GMT  
		Size: 38.2 MB (38208676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99adf624c49fbc793f98ee755fbe0ab94d745f3f25bf27a9d776205f11d26731`  
		Last Modified: Tue, 20 Jan 2026 21:10:54 GMT  
		Size: 30.9 MB (30859138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef57dd41ed14d4f3124d43da161e0f90b08d6fdd0d9d730a0705ad0365f0dba4`  
		Last Modified: Tue, 20 Jan 2026 21:11:00 GMT  
		Size: 143.7 MB (143685283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a282a441a280c3a1e17a2e2820d7105b84fb9992fb7cced6e6cb84414e1372`  
		Last Modified: Tue, 20 Jan 2026 19:15:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b787ea9a3bd62699117a68cf6f019cb7557f09bf0ccb4820fc0e76612383f646`  
		Last Modified: Tue, 20 Jan 2026 19:15:23 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f953c5268a83c902ccb1295521be86702468921409e7e4ccee15a339a854f2e2`  
		Last Modified: Wed, 21 Jan 2026 00:03:05 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f0006662ce8827a1c53943d51d4c6bc4cc0cd6acaa5409763e9d81ead8b897`  
		Last Modified: Tue, 20 Jan 2026 21:12:16 GMT  
		Size: 36.1 MB (36060203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7613fc360ff1050c0fbf8a9b94cccec3dfc51df8e1c1c8a84073fadd8187a039`  
		Last Modified: Tue, 20 Jan 2026 21:12:09 GMT  
		Size: 128.5 MB (128469424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f2720af9be2e912f12cf0d26c5a62f9249996fbbaf70354f4667d1425ac03c3`  
		Last Modified: Tue, 20 Jan 2026 21:12:06 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:d4735a0d759788472135b9c4180afe6e708b85ac7281679d766f0574a75d6146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46deef7a4dd9068f3b3846e181c594fe427c89d8f089810c9b2e8916948bd966`

```dockerfile
```

-	Layers:
	-	`sha256:55b1bbce80d2cac91c73d87c7735f354cbb40522cd3b4552447131332bd7ef8f`  
		Last Modified: Wed, 21 Jan 2026 00:19:36 GMT  
		Size: 5.3 MB (5312626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12945067103a12a56795113f044c83ce6c1b038cdfdc3a00fb4b83c6ba233eb9`  
		Last Modified: Tue, 20 Jan 2026 21:12:05 GMT  
		Size: 23.7 KB (23720 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:303402f149850e1c452b72eddeab12a681d5fdaa4822e9ffdf5c7720d522eb39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 MB (388374410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8aab17c8fb6fd007fa949109322d6454dca5709aa62e5feeaf095308c03d741`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 01:08:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 01:08:41 GMT
ENV container oci
# Mon, 19 Jan 2026 01:08:42 GMT
COPY dir:3bd7ec6f425d769a16814adff3b957a15c4cbdec659c93cd45b1a546561564a3 in /      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 01:08:42 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:42 GMT
COPY file:fe8dfccf0fa987a5d4946f1b72ab0cc09a6e656396d24bdd16b87ea3307e9302 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 01:08:43 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T01:08:31Z" "org.opencontainers.image.created"="2026-01-19T01:08:31Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T01:08:31Z
# Tue, 20 Jan 2026 19:12:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:12:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:12:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:12:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:12:37 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 20 Jan 2026 19:15:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Jan 2026 19:15:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:15:56 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:15:56 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Jan 2026 19:15:56 GMT
CMD ["jshell"]
# Tue, 20 Jan 2026 21:10:47 GMT
CMD ["gradle"]
# Tue, 20 Jan 2026 21:10:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 20 Jan 2026 21:10:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 20 Jan 2026 21:10:47 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 20 Jan 2026 21:10:48 GMT
WORKDIR /home/gradle
# Tue, 20 Jan 2026 21:13:50 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 20 Jan 2026 21:13:50 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 20 Jan 2026 21:13:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 20 Jan 2026 21:18:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 20 Jan 2026 21:18:51 GMT
USER gradle
# Tue, 20 Jan 2026 21:18:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 20 Jan 2026 21:18:53 GMT
USER root
```

-	Layers:
	-	`sha256:cb3df95d99fa30c8131b824671f0e15d0c34235a2e7bda21e4a361d100760346`  
		Last Modified: Mon, 19 Jan 2026 06:13:44 GMT  
		Size: 44.5 MB (44459713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c7d8e1a879073a2bb5883fd40b014f62a8e14ba675ff25067ab8b020299f7b`  
		Last Modified: Tue, 20 Jan 2026 19:13:32 GMT  
		Size: 32.9 MB (32898320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ea9aff93f7a2d4b766588c86e1f636908fbb268f889c1a0dae3792ed8c9892`  
		Last Modified: Wed, 21 Jan 2026 02:53:42 GMT  
		Size: 144.5 MB (144547841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f11c16a049968f9a09c4a82e01c0d11329593e770fd640b186781d212a3eaf`  
		Last Modified: Tue, 20 Jan 2026 19:16:52 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9637a2029506668c96d0da940d23a567b179612d3db74b5399330993178e9f`  
		Last Modified: Tue, 20 Jan 2026 19:15:59 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e546af418afe975468a14b6cc25ba601ee3d4faf3a1ac659cc9990be7b32daa`  
		Last Modified: Tue, 20 Jan 2026 21:12:42 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c742aead0ce5879244961d54cf110d13c00fb8c579cd045d98780531ec41f401`  
		Last Modified: Wed, 21 Jan 2026 03:59:48 GMT  
		Size: 38.0 MB (37959939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1604c6f1bd06d300baaa467b257444da6b0987fc04075a60988bfe46756a52e`  
		Last Modified: Wed, 21 Jan 2026 04:00:21 GMT  
		Size: 128.5 MB (128469424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72669579354b306adec94ea815028ae662dfb591da2f22fc143db8ce679abfdf`  
		Last Modified: Tue, 20 Jan 2026 21:20:04 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:290f714eb8b2a3ccb0b9b88e55275e8a43459da16a103fd8b9d6443be999d8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a9443e96f670b75b98282ff856d4a74b596972cc618d7eb027d1e5985318cf`

```dockerfile
```

-	Layers:
	-	`sha256:f2ef124cf7493481b9e5b051eaac1f142eb3a0621f5b8fdc3fd8953561a648f2`  
		Last Modified: Wed, 21 Jan 2026 00:19:39 GMT  
		Size: 5.3 MB (5310543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7c005feccb4f8aa0b5707927ddb07fed7170173ebf6dbd46325f046395b7da3`  
		Last Modified: Wed, 21 Jan 2026 00:19:39 GMT  
		Size: 23.6 KB (23645 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:51f7c4c0dbf75ba16b2966fdd41c3dac8c486131dc6dfa2c380c1b62d68923e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368292525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52363ce2dbbfa9d1dd46fd340d541247d44d22b7ea62f2ffa8d68413a0124ac6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 19 Jan 2026 00:56:30 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:34 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 19 Jan 2026 00:56:38 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 19 Jan 2026 00:56:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 19 Jan 2026 00:56:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 19 Jan 2026 00:56:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 19 Jan 2026 00:56:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:57:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 19 Jan 2026 00:57:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 19 Jan 2026 00:57:08 GMT
ENV container oci
# Mon, 19 Jan 2026 00:57:08 GMT
COPY dir:60e8b920663668133ad1c0beb8ddee0ed0404da0ad2cb12d0bdf023f3692297c in /      
# Mon, 19 Jan 2026 00:57:08 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 19 Jan 2026 00:57:08 GMT
CMD ["/bin/bash"]
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:3606e23b291d122a467fe42706adc9bb412f4262f39a03046011b69272713a85 in /usr/share/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:57:09 GMT
COPY file:3606e23b291d122a467fe42706adc9bb412f4262f39a03046011b69272713a85 in /root/buildinfo/labels.json      
# Mon, 19 Jan 2026 00:57:09 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "org.opencontainers.image.revision"="d9151f7dd4dfe1cc8a2df524b85cddd483628d5e" "build-date"="2026-01-19T00:56:09Z" "org.opencontainers.image.created"="2026-01-19T00:56:09Z" "release"="1768783948"org.opencontainers.image.revision=d9151f7dd4dfe1cc8a2df524b85cddd483628d5e,org.opencontainers.image.created=2026-01-19T00:56:09Z
# Tue, 20 Jan 2026 19:11:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Jan 2026 19:11:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Jan 2026 19:11:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Jan 2026 19:11:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 20 Jan 2026 19:11:50 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Tue, 20 Jan 2026 19:11:56 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Jan 2026 19:11:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Jan 2026 19:11:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Jan 2026 19:11:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Jan 2026 19:11:57 GMT
CMD ["jshell"]
# Tue, 20 Jan 2026 21:09:59 GMT
CMD ["gradle"]
# Tue, 20 Jan 2026 21:09:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 20 Jan 2026 21:09:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 20 Jan 2026 21:09:59 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 20 Jan 2026 21:09:59 GMT
WORKDIR /home/gradle
# Tue, 20 Jan 2026 21:11:10 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 20 Jan 2026 21:11:10 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 20 Jan 2026 21:11:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 20 Jan 2026 21:11:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 20 Jan 2026 21:11:14 GMT
USER gradle
# Tue, 20 Jan 2026 21:11:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 20 Jan 2026 21:11:14 GMT
USER root
```

-	Layers:
	-	`sha256:8d0fd9f50ed7506edfb499eb958eedd9d04f1fe7d6ebb11e4c454c579c856a27`  
		Last Modified: Mon, 19 Jan 2026 06:13:30 GMT  
		Size: 38.1 MB (38120160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c1899ea409ad5dc72be7103ffc18eadcabc3eed0be0dc073945f83328d91a3`  
		Last Modified: Tue, 20 Jan 2026 21:11:33 GMT  
		Size: 30.5 MB (30452733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35287b45fb3b19b6b184a48f042b4eaa70e6a26d477c5c35624aeddd2c14fca`  
		Last Modified: Tue, 20 Jan 2026 19:12:23 GMT  
		Size: 134.9 MB (134862227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ae95ec2853e3d0938bb0366ae5a68112b98b59dcf51505f5c13509d201104a`  
		Last Modified: Tue, 20 Jan 2026 19:12:20 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859ece53b3bb0316b1dc44ab784808b01e8cdc28e3ad4fe3af2b7a695a3c8c9b`  
		Last Modified: Tue, 20 Jan 2026 19:12:20 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453cefb3cd755f0201b02d44889ce198ff8fec947ba766d39f96c83ea1278e45`  
		Last Modified: Tue, 20 Jan 2026 21:10:49 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12bf439a41c6e0d377189dc6afbbb50ae8a391c8786b92211514e76f75da0e6`  
		Last Modified: Tue, 20 Jan 2026 21:11:39 GMT  
		Size: 36.3 MB (36348821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e309ebb9e74c4c0983a9ba2ffa20227fee96a7ab535a4a50a57bb570a4e0be`  
		Last Modified: Tue, 20 Jan 2026 22:12:45 GMT  
		Size: 128.5 MB (128469422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396382a99b868d07d2df828c90937de6aa37713c31eb64e80b1682523c890b0e`  
		Last Modified: Tue, 20 Jan 2026 21:11:46 GMT  
		Size: 35.0 KB (35001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:9b4a7e17c7b9ce647e9111c753be095a1f74a851da9e93a38552c2466ec401a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba99173cd7c12ae975b4604c3ae0f696d27239884ec95313f3986191c801e08f`

```dockerfile
```

-	Layers:
	-	`sha256:966c2d12dd9fd4fcb170591b8743d21374cf63948c767030246f93b5e7f5634c`  
		Last Modified: Wed, 21 Jan 2026 00:19:44 GMT  
		Size: 5.3 MB (5299829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6bce9dfcbd959aa8730f8d87d74dc2be30bda7e6aa036da8822db2b15d7ff9`  
		Last Modified: Tue, 20 Jan 2026 21:11:37 GMT  
		Size: 23.6 KB (23583 bytes)  
		MIME: application/vnd.in-toto+json
