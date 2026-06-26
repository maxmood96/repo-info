## `gradle:6-jdk11-ubi`

```console
$ docker pull gradle@sha256:cc410731afc4719037f56a6c43f8eeeb93a5eabeba48cabefc1710e7e1e03f1a
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

### `gradle:6-jdk11-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:4cec70c8bc89c261d390f423919a4234bf471efeb030bd1c6c1db364e9ab1af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.7 MB (356748451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce813cd6d3a5f48ca3b8d19015e30ef3d56ce4a1c65d83c670edc46350739f2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:47:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:47:54 GMT
ENV container oci
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:a7d61486b18f71651e6d0b0c0267c96964cdf86a5c99a34dafc1bfd05eac4cc1 in /      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:47:55 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
COPY dir:bc9ddd3d40bc004a03f930c7616b544996fd5453e30f14853f7ba4b54693ba2e in /root/buildinfo/      
# Thu, 25 Jun 2026 05:47:55 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:47:36Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:47:36Z" "architecture"="x86_64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:47:36Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:26:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:26:43 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:43 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Thu, 25 Jun 2026 23:26:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:26:51 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:26:51 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:26:51 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:51 GMT
CMD ["jshell"]
# Fri, 26 Jun 2026 00:13:12 GMT
CMD ["gradle"]
# Fri, 26 Jun 2026 00:13:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 26 Jun 2026 00:13:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 26 Jun 2026 00:13:12 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 26 Jun 2026 00:13:12 GMT
WORKDIR /home/gradle
# Fri, 26 Jun 2026 00:13:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 26 Jun 2026 00:13:16 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 26 Jun 2026 00:13:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 26 Jun 2026 00:13:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 26 Jun 2026 00:13:18 GMT
USER gradle
# Fri, 26 Jun 2026 00:13:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 26 Jun 2026 00:13:18 GMT
USER root
```

-	Layers:
	-	`sha256:837b9d7bd4c8301d318ec8c5cd7e5aab81e392d60e90b733f39c67bbadc97aef`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 40.7 MB (40689274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fa9388d153eea89d27cc9cb65c1e5b139c0dc983a46487113e3c84b7d17c67`  
		Last Modified: Thu, 25 Jun 2026 23:27:07 GMT  
		Size: 27.7 MB (27660456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997c8384ae39ef792d7e9905484e365842cd37078d47190ddae2a0fe7dd2c85c`  
		Last Modified: Thu, 25 Jun 2026 23:27:09 GMT  
		Size: 142.3 MB (142348849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bec63b8789a281cbba80d5c90cfaef00a091d49c43f2caf465235ed1d7ce8bc`  
		Last Modified: Thu, 25 Jun 2026 23:27:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a95a5e66938d247097535e76596dc55e0c99dc0882d8db114259c567138029`  
		Last Modified: Thu, 25 Jun 2026 23:27:06 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e63452b1363f31c5e7ae41a86a74b1f8728b3a075af808d3c6e68b5e06de35`  
		Last Modified: Fri, 26 Jun 2026 00:13:34 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97376554182bc2d57fcdf52bc8f0be405c1f7552205b03dd6fe2d4a4898cbcc`  
		Last Modified: Fri, 26 Jun 2026 00:13:36 GMT  
		Size: 37.9 MB (37917769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4381b10b7682f8534af88f7fafbd2cd03c7cdea0b8b1d6d07224be27f2c01f2f`  
		Last Modified: Fri, 26 Jun 2026 00:13:38 GMT  
		Size: 107.7 MB (107696667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f0d8f4bf19728e0e0601d93fbd9a6494d79d7b24d8061bda33862cc26101c7`  
		Last Modified: Fri, 26 Jun 2026 00:13:34 GMT  
		Size: 431.3 KB (431271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:aa099f69996d0e607f83619df40716c5462d02cbfff236359bd009f4e8db23e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a026c9149a270399fe3a72584b797a134afe3ecdcf51e457ed92263610433470`

```dockerfile
```

-	Layers:
	-	`sha256:520616cca1155cdc2bbf18fb93e404968ddcba2bd7ee1400a13c9e6ab657fc76`  
		Last Modified: Fri, 26 Jun 2026 00:13:34 GMT  
		Size: 5.3 MB (5318732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cac2f9e5e1e37c3dda6dd0d21aade2e9ae8aa45fbdfb69ed246b9523ab9c826`  
		Last Modified: Fri, 26 Jun 2026 00:13:34 GMT  
		Size: 23.5 KB (23548 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b451a34a67c896550c95a35087e0535a884cff17a9152ffc5f183e4e7269412b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351286437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd460356053bd43b659d08165d8c33f2969ea9928bb6cf4e544f5da81ecae747`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:52 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b536f0b76258d9997dadb73f000a4dcb4ac61a94c87f2002404cf80795af1987 in /      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:53 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:53 GMT
COPY dir:b92b494a8ba7f60e9dc6ef43f3b9b86d3f1fe0910e706399a14b6f518777f64a in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:54 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:49:31Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:49:31Z" "architecture"="aarch64" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:49:31Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:25:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:25:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:25:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:25:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:25:59 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Thu, 25 Jun 2026 23:26:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:26:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:26:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:26:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:26:08 GMT
CMD ["jshell"]
# Fri, 26 Jun 2026 00:12:27 GMT
CMD ["gradle"]
# Fri, 26 Jun 2026 00:12:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 26 Jun 2026 00:12:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 26 Jun 2026 00:12:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 26 Jun 2026 00:12:27 GMT
WORKDIR /home/gradle
# Fri, 26 Jun 2026 00:12:30 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 26 Jun 2026 00:12:30 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 26 Jun 2026 00:12:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 26 Jun 2026 00:12:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 26 Jun 2026 00:12:33 GMT
USER gradle
# Fri, 26 Jun 2026 00:12:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 26 Jun 2026 00:12:33 GMT
USER root
```

-	Layers:
	-	`sha256:f224574d4b82cf6adf57df98fdab92768ce7f1579fbe0678919b872f4d435c0e`  
		Last Modified: Thu, 25 Jun 2026 06:49:07 GMT  
		Size: 38.8 MB (38818113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ead1d70b0a5aa89fbde06eab197ad2871fb2f44f7ef3f9d5676e0cfe8d85c7e`  
		Last Modified: Thu, 25 Jun 2026 23:26:25 GMT  
		Size: 28.1 MB (28100592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ac721bdbf4348852995d6395fd9787a0e170daddee0ddbe5d34c75a0488ded`  
		Last Modified: Thu, 25 Jun 2026 23:26:28 GMT  
		Size: 139.0 MB (139040650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14db36fba366d8ca287d2f68ac13bdae50a08fff6efcd304257fb62283dc88a9`  
		Last Modified: Thu, 25 Jun 2026 23:26:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae8b82e839a3f85164e5818dadd575dce556c493de876c0655bfe6f16db57d0`  
		Last Modified: Thu, 25 Jun 2026 23:26:24 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b378a4cb5335ab2da56bb92e954c0c69509744c652fef4e2bd03d705fe4778f`  
		Last Modified: Fri, 26 Jun 2026 00:12:49 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889bf60147f680361301eeed82bc662de65e6429bcbeb09027529b12e73078f7`  
		Last Modified: Fri, 26 Jun 2026 00:12:51 GMT  
		Size: 37.2 MB (37201232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b47e27cbffe7cb75de632889ea6f6dfd3dc8e0d6fd1b74c0e50d8f58ed3c923`  
		Last Modified: Fri, 26 Jun 2026 00:12:53 GMT  
		Size: 107.7 MB (107696670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ca1eb2761799ccc5edf2258be269ca1f1e1fc9830be103ea8b1ef1b72261d2`  
		Last Modified: Fri, 26 Jun 2026 00:12:49 GMT  
		Size: 425.0 KB (425020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:9407136e5da7b8b62ae06fcdbf222b93a40d6263e6a5d07807066ddd02f68702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5340695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ac4b61f8a192a8d8ff68473c5df95ab123849d30b924eabaf722448dd6dcf2`

```dockerfile
```

-	Layers:
	-	`sha256:5ed02b662282454e596feb50ea62ec3887907cf003a21de56bc82fda95e42ce7`  
		Last Modified: Fri, 26 Jun 2026 00:12:49 GMT  
		Size: 5.3 MB (5316974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc15db6e81f469cfaddd5f48c54979b818c298e6ef89feadfa7bee7536eee74`  
		Last Modified: Fri, 26 Jun 2026 00:12:49 GMT  
		Size: 23.7 KB (23721 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:54441b5ab0dbce12f82ba8922c42d88c8f09f74aaf5779b7ddb2278c7752391d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351688553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f1888851e4d1406f937fa138ca9a9ddd2ddef8bd148008f1d9ef8438a9dd0a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:49:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:49:04 GMT
ENV container oci
# Thu, 25 Jun 2026 05:49:05 GMT
COPY dir:f90c99a59bd474ed6a51399eee7df05393563fdaaa902130421d08a1a3fedeec in /      
# Thu, 25 Jun 2026 05:49:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:49:05 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:49:05 GMT
COPY dir:cb70b1c584e490eac8673058fb514f718bb38524b957a3c5934b6749eca2ca95 in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:49:05 GMT
COPY dir:cb70b1c584e490eac8673058fb514f718bb38524b957a3c5934b6749eca2ca95 in /root/buildinfo/      
# Thu, 25 Jun 2026 05:49:05 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:48:49Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:48:49Z" "architecture"="ppc64le" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:48:49Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:26:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:26:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:26:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:26:15 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:26:15 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Thu, 25 Jun 2026 23:27:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:27:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:27:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:27:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:27:16 GMT
CMD ["jshell"]
# Fri, 26 Jun 2026 00:12:01 GMT
CMD ["gradle"]
# Fri, 26 Jun 2026 00:12:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 26 Jun 2026 00:12:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 26 Jun 2026 00:12:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 26 Jun 2026 00:12:02 GMT
WORKDIR /home/gradle
# Fri, 26 Jun 2026 00:13:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 26 Jun 2026 00:13:27 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 26 Jun 2026 00:13:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 26 Jun 2026 00:14:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 26 Jun 2026 00:14:32 GMT
USER gradle
# Fri, 26 Jun 2026 00:14:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 26 Jun 2026 00:14:34 GMT
USER root
```

-	Layers:
	-	`sha256:1ce5d05f6e5641b082a71f1e9acc2940448540498097c2a35b74cf93310f5178`  
		Last Modified: Thu, 25 Jun 2026 12:13:27 GMT  
		Size: 45.1 MB (45075525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454ffa9ad55609063881c74aef17705d7d65e97d1f5ceadb3fe8c414ff22b193`  
		Last Modified: Thu, 25 Jun 2026 23:26:50 GMT  
		Size: 30.1 MB (30082746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c59df5e5dad962af740ef6ae40ffed6e3a020fce1e40545841f648f1c9df4fe`  
		Last Modified: Thu, 25 Jun 2026 23:27:49 GMT  
		Size: 129.6 MB (129614206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ef4ec99590fdce55b39978d5fae9980f8e7c6ef81d199931d88197f79c5712`  
		Last Modified: Thu, 25 Jun 2026 23:27:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0894843b50fafbe045b3e0da22d559d7b0fc8c4087b9fe02dd723fe957f10b5b`  
		Last Modified: Thu, 25 Jun 2026 23:27:29 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4d5418d782499dfdc8205f5076058f61ab83c022ba9022e24e2c39c65f2a78`  
		Last Modified: Fri, 26 Jun 2026 00:12:54 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e268cfb06899880a16db1d8e4748e2d7d42616b835112f7ca9896299ac159abf`  
		Last Modified: Fri, 26 Jun 2026 00:14:15 GMT  
		Size: 39.2 MB (39180262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4a885edad207e358ed5cb5c9fa4404e8fb5100f6698ffcc5b26477a893b2ed`  
		Last Modified: Fri, 26 Jun 2026 00:15:05 GMT  
		Size: 107.7 MB (107696669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75b029f0a8be3da37d9ef659edf984e7840c71b65910b9ec836b4943ecc49e7`  
		Last Modified: Fri, 26 Jun 2026 00:15:02 GMT  
		Size: 35.0 KB (34983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1ba163c6a581d400591661c78c5dada8f71e5704f4c8494c8d8ae6ca722f8b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878dc113c97591d225c49f0b20cb6276d638674991bdeab25ef428f676fbcabf`

```dockerfile
```

-	Layers:
	-	`sha256:bc9ee63ec1f69682c3140872264596f20b03745f58759c209f36ef88767fa168`  
		Last Modified: Fri, 26 Jun 2026 00:15:02 GMT  
		Size: 5.3 MB (5313696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f489d540a597734f911fcb8ce23d1fd384f99281a7164bf5c9bd3eee10e46e`  
		Last Modified: Fri, 26 Jun 2026 00:15:01 GMT  
		Size: 23.6 KB (23645 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:d3c6b09b63b7317a67de87297d4a15f02b3a52d85d0f8323606630400b11b834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.7 MB (334736625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9702b6c2603277d30cda9d716ed630a65f7d0e93af884a59a73c8bdfc5e6137`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.openshift.expose-services=""
# Thu, 25 Jun 2026 05:52:27 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 25 Jun 2026 05:52:27 GMT
ENV container oci
# Thu, 25 Jun 2026 05:52:27 GMT
COPY dir:1e4f533284314158fe9071edbf6e5a91d133d00a252b00de728bc4926b26b337 in /      
# Thu, 25 Jun 2026 05:52:27 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 25 Jun 2026 05:52:27 GMT
CMD ["/bin/bash"]
# Thu, 25 Jun 2026 05:52:27 GMT
COPY dir:5b21c0bd8fdb721477bc5c6da5a748382232df7791527a89e418bc39ef6e03ed in /usr/share/buildinfo/      
# Thu, 25 Jun 2026 05:52:28 GMT
COPY dir:5b21c0bd8fdb721477bc5c6da5a748382232df7791527a89e418bc39ef6e03ed in /root/buildinfo/      
# Thu, 25 Jun 2026 05:52:28 GMT
LABEL "org.opencontainers.image.created"="2026-06-25T05:51:47Z" "org.opencontainers.image.revision"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "build-date"="2026-06-25T05:51:47Z" "architecture"="s390x" "vcs-ref"="b76cbbe03678b6bed00cb452eb031ce6d202c981" "vcs-type"="git" "release"="1782366411"org.opencontainers.image.created=2026-06-25T05:51:47Z,org.opencontainers.image.revision=b76cbbe03678b6bed00cb452eb031ce6d202c981
# Thu, 25 Jun 2026 23:24:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jun 2026 23:24:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jun 2026 23:24:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 25 Jun 2026 23:24:56 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 25 Jun 2026 23:24:56 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Thu, 25 Jun 2026 23:25:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 25 Jun 2026 23:25:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 25 Jun 2026 23:25:04 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 25 Jun 2026 23:25:04 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 25 Jun 2026 23:25:04 GMT
CMD ["jshell"]
# Fri, 26 Jun 2026 00:11:16 GMT
CMD ["gradle"]
# Fri, 26 Jun 2026 00:11:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 26 Jun 2026 00:11:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 26 Jun 2026 00:11:16 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 26 Jun 2026 00:11:16 GMT
WORKDIR /home/gradle
# Fri, 26 Jun 2026 00:11:20 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 26 Jun 2026 00:11:20 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 26 Jun 2026 00:11:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 26 Jun 2026 00:11:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 26 Jun 2026 00:11:25 GMT
USER gradle
# Fri, 26 Jun 2026 00:11:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 26 Jun 2026 00:11:25 GMT
USER root
```

-	Layers:
	-	`sha256:601b4838142f06d7d4e767a327592a762187b9af6287ad5286218612b47da08f`  
		Last Modified: Thu, 25 Jun 2026 12:13:18 GMT  
		Size: 38.7 MB (38740623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13318bf4eac76cd98e559c9948f545e02787bc71d84cc1c6e26cac00f3ccd433`  
		Last Modified: Thu, 25 Jun 2026 23:25:34 GMT  
		Size: 27.7 MB (27684193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f528ee9e8e5423525905e1d821789b2edc4b587ab9b9550e722db8d67ad6fbe2`  
		Last Modified: Thu, 25 Jun 2026 23:25:36 GMT  
		Size: 123.1 MB (123061372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb28bde086b2d0a099966912a797b8d79ad599465febfae1768d1c29d569ac9d`  
		Last Modified: Thu, 25 Jun 2026 23:25:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd975bbc31a44531aa72e676ae0c97ce8dd92c454eb3cff1dffa5a266ed12c9`  
		Last Modified: Thu, 25 Jun 2026 23:25:34 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52773e7b9209da3f34d9e0ee0c80defcb25c623552b88d57ffc08b03334a748`  
		Last Modified: Fri, 26 Jun 2026 00:11:52 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc06b478908b04a625da5a369ed288eff247040b5df898792ca0f7e0a597526`  
		Last Modified: Fri, 26 Jun 2026 00:11:54 GMT  
		Size: 37.5 MB (37514629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93814c2a636a1c9ff7b2a18b3097ca3483c6b15b45f83e202ee6f18f21938898`  
		Last Modified: Fri, 26 Jun 2026 00:11:56 GMT  
		Size: 107.7 MB (107696670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5113abcb8dbba3da60d071b592517034d5a6fda9def834bdab6e26e15518ae`  
		Last Modified: Fri, 26 Jun 2026 00:11:52 GMT  
		Size: 35.0 KB (34977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:b6f012cde382cb2af87b9fc5b9b260bc9a0b9e5896c157e9a0a28bd6b1929747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa063adfce397a0f35392e57a342a502e4064167959b24c0d5792dd3104cc17`

```dockerfile
```

-	Layers:
	-	`sha256:1fe98707dbe655aab6aa2ea84fcfa90fb37c1024a8a4d3d54dac74d9e694a8d5`  
		Last Modified: Fri, 26 Jun 2026 00:11:52 GMT  
		Size: 5.3 MB (5303559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ba2ca22754533cd7f708446cfdbaf679c261f1cc36dc328ceb7fe273e24bc5e`  
		Last Modified: Fri, 26 Jun 2026 00:11:51 GMT  
		Size: 23.6 KB (23583 bytes)  
		MIME: application/vnd.in-toto+json
