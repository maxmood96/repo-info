## `gradle:9-jdk21-ubi10`

```console
$ docker pull gradle@sha256:ab96932065660ddb35867cd7dce8404fd45a925c2d5c373a07e8c1230526063c
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

### `gradle:9-jdk21-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:223aeda7ca43da44f198a2b5f7ffae2972670fd28fa6bc04f563588d56316b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.2 MB (410226363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3bdd9c0d2f3872f8d078abd24f488f44e8fb7a85d32765c9ba17c3942f2d27`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:36:53 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:36:53 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:36:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:36:53 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:36:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:36:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:36:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:36:53 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:36:53 GMT
ENV container oci
# Mon, 04 May 2026 01:36:54 GMT
COPY dir:90d4f1f85494d2a8bf17340af60eb04fb8df2adbe40376c2198b52d03b3dce87 in /      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:36:54 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:36:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:44acb722ff6847a849911ad1532360393cd9c16592e8d1f9e199cff925bbc7d5 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:36:54 GMT
COPY file:44acb722ff6847a849911ad1532360393cd9c16592e8d1f9e199cff925bbc7d5 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:36:54 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:36:38Z" "org.opencontainers.image.created"="2026-05-04T01:36:38Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:36:38Z
# Tue, 05 May 2026 23:08:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:14 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 05 May 2026 23:08:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:42 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:11:50 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:11:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:11:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:11:50 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:11:50 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:11:56 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:11:56 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 00:11:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Wed, 06 May 2026 00:11:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:11:59 GMT
USER gradle
# Wed, 06 May 2026 00:11:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 06 May 2026 00:11:59 GMT
USER root
```

-	Layers:
	-	`sha256:6c2848906904fdb30be3302af6950faf3bb49f8acf1fe7da43266ab561f76092`  
		Last Modified: Mon, 04 May 2026 03:13:50 GMT  
		Size: 34.6 MB (34648199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18b8fd3323a4e72d45f54bc20f5d7b1d3faff4ea3989c5f1c27e7c27650909c`  
		Last Modified: Tue, 05 May 2026 23:08:29 GMT  
		Size: 22.0 MB (22037273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce83d96d62df3ff9849f8968920733bffe952aed77019b41b6cdcd81ab7454fc`  
		Last Modified: Tue, 05 May 2026 23:09:00 GMT  
		Size: 157.9 MB (157861023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeebc903b2ce96d9e7be6f0aa2606171dc645ff433684a7abf23b21218fef7a1`  
		Last Modified: Tue, 05 May 2026 23:08:57 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ad78efc9601357a49c351e13747cf68855464bb3fa6e80924162167a6dfc70`  
		Last Modified: Tue, 05 May 2026 23:08:57 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25192e75914abc65931c60da6bfac3648b5403d0947f142a27a9faedf0f8d90c`  
		Last Modified: Wed, 06 May 2026 00:12:20 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f874f84b8b2d607f22719a09db597333dff8bdbf11bbc882f1a40b8023fac30`  
		Last Modified: Wed, 06 May 2026 00:12:25 GMT  
		Size: 55.4 MB (55414432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe7624c9a68164ba6b6584146d2b878e61017e453ef8c4384cf6612640f243`  
		Last Modified: Wed, 06 May 2026 00:12:27 GMT  
		Size: 140.2 MB (140235928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235428e880d2d6c515e1168c5ce260457fdd38df9809b25b3b37f2830928143a`  
		Last Modified: Wed, 06 May 2026 00:12:21 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:50d9d377503ece7dcee110372f6ccb5bfbc311231d23936060246661b5f78d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7084590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f50db1fdb4ca82f1da8006840faf25844d1537fb1efa565bf721467df416e0e`

```dockerfile
```

-	Layers:
	-	`sha256:a8a10570f097622f1471e92f55bbab8497ad7593f9ea1af8a8c161b5d2b73188`  
		Last Modified: Wed, 06 May 2026 00:12:21 GMT  
		Size: 7.1 MB (7060139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65696cd99b8d7603cc348b8ae7ac2800d301a2cf90d7d815c2e69dc8c17047f1`  
		Last Modified: Wed, 06 May 2026 00:12:20 GMT  
		Size: 24.5 KB (24451 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e77d95c97bff9a0513161efb2a8e20f5f0dc7494d2d8b06e6d363468ba972f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.0 MB (406000736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b827efa591283e82edf74c3a25c30d7fbb0148667663480a411e41c44c0df19d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:38:51 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:38:51 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:38:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:38:51 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:38:51 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:38:51 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:38:51 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:38:51 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:38:51 GMT
ENV container oci
# Mon, 04 May 2026 01:38:52 GMT
COPY dir:4f490e44b5cd259c269df4e89626a736e4b70875a47bc79b960d52f7b56f7967 in /      
# Mon, 04 May 2026 01:38:52 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:38:52 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:38:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:38:52 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:38:53 GMT
COPY file:e2c2a2ab213ef0433a1e15d666daa6e664714283c2d03394bbfa240f7cd44679 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:38:53 GMT
COPY file:e2c2a2ab213ef0433a1e15d666daa6e664714283c2d03394bbfa240f7cd44679 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:38:53 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:38:35Z" "org.opencontainers.image.created"="2026-05-04T01:38:35Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:38:35Z
# Tue, 05 May 2026 23:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:13 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 05 May 2026 23:08:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:22 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:11:39 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:11:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:11:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:11:39 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:11:39 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:11:45 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:11:45 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 00:11:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Wed, 06 May 2026 00:11:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:11:48 GMT
USER gradle
# Wed, 06 May 2026 00:11:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 06 May 2026 00:11:49 GMT
USER root
```

-	Layers:
	-	`sha256:908809553a77ac560aff532a902be43c3a99a0dcb4f759158a75984cb82c4b9d`  
		Last Modified: Mon, 04 May 2026 06:16:39 GMT  
		Size: 32.7 MB (32711611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69245fcf4f18604802b067e726477bdeadade80142d6cddb68d199c37158d038`  
		Last Modified: Tue, 05 May 2026 23:08:41 GMT  
		Size: 22.3 MB (22301730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4ccd990a06f99231ae975c07d6e49b46b796d0eed8711614662c37e6f36ce9`  
		Last Modified: Tue, 05 May 2026 23:08:44 GMT  
		Size: 156.1 MB (156136240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90ea0166f25ae94800ac7c9f80fd970494654edc9b86f6c94805c7ebedf56cd`  
		Last Modified: Tue, 05 May 2026 23:08:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec41f2dc173160877196ba1cd7920c934714831abfaa25d71161dabe295c68d`  
		Last Modified: Tue, 05 May 2026 23:08:40 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c694abfe327d2bc19f41b056c6ea470940b9fd1f62b2ba43464eeca056311169`  
		Last Modified: Wed, 06 May 2026 00:12:10 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e466c41a196e1c2524502e820640304afba0eb0f4c3f3d4bd4b3dc3af5e00d0`  
		Last Modified: Wed, 06 May 2026 00:12:12 GMT  
		Size: 54.6 MB (54581969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3046914ad292e0505f045085f0e30a3b5b1fc6f0f852243a7d2f2297a6cef2`  
		Last Modified: Wed, 06 May 2026 00:12:14 GMT  
		Size: 140.2 MB (140235945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8865742e6e63a4855afd9a406813ac0cc365af69aa7a9f72b750c0df3088b6b7`  
		Last Modified: Wed, 06 May 2026 00:12:09 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:135f841e10b6faf8fc786cb06a6ff215354dfd7b65b2471c6cdc2625e4a4d85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7083043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4279a948a0288fc524fe43f5067821623ea746601c2cc67b82353647f18131f`

```dockerfile
```

-	Layers:
	-	`sha256:020016a63923ad6fe4ccb4bee308bda26e4d8bcf7a5db1098089c3e2973e371d`  
		Last Modified: Wed, 06 May 2026 00:12:10 GMT  
		Size: 7.1 MB (7058395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630dc5da0c6a66c851950dfbd3274d2940c62f240a97b06e61480e74b2b60a2c`  
		Last Modified: Wed, 06 May 2026 00:12:10 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:47481a879eaf5653c7cbbd497f4f25eada45fb2d306dd25344eac69e156cabf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.1 MB (418053705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429e3e92480ea192bb2d7be2496778cd6c5004c3f8cd75186f4c367819e22af5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:39:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:39:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:39:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:39:14 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:39:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:39:15 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:39:15 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:39:15 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:39:15 GMT
ENV container oci
# Mon, 04 May 2026 01:39:15 GMT
COPY dir:12413a5bdb80a75f63d061b3c0328d3ec0033dbb6ef2e4efcba8481b6ce277c7 in /      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:39:15 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:39:15 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:39:15 GMT
COPY file:727a91663c7c1ef3c87416ec38b4c09702b0fa948721f73b1c8c27f7a242068b in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:39:16 GMT
COPY file:727a91663c7c1ef3c87416ec38b4c09702b0fa948721f73b1c8c27f7a242068b in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:39:16 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:39:03Z" "org.opencontainers.image.created"="2026-05-04T01:39:03Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:39:03Z
# Tue, 05 May 2026 23:47:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:47:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:47:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:47:29 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 05 May 2026 23:53:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:53:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:53:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:53:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:53:55 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:15:17 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:15:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:15:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:15:17 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:15:17 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:15:55 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:15:55 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 00:15:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Wed, 06 May 2026 00:16:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:16:02 GMT
USER gradle
# Wed, 06 May 2026 00:16:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 06 May 2026 00:16:04 GMT
USER root
```

-	Layers:
	-	`sha256:f2dd1d2c3d5fda579799f9becd292589fb99f0abc7f5c226856eb2bbbbc120cc`  
		Last Modified: Mon, 04 May 2026 06:16:51 GMT  
		Size: 38.7 MB (38745905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2ee71f34837c204e126c0f30bd59bdd1c1aad2d6a82e82078b6ce249102e06`  
		Last Modified: Tue, 05 May 2026 23:48:16 GMT  
		Size: 23.3 MB (23333693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b4df0c2151351f00b86bf904ed4374865dbadbc083c18fed8da6815c15a621`  
		Last Modified: Tue, 05 May 2026 23:54:32 GMT  
		Size: 158.0 MB (157981346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332691c767ddeebd25911f2bc535b63db93ea983d894b5e7467f27679c099ea3`  
		Last Modified: Tue, 05 May 2026 23:54:28 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab1b51621c97c389da0f0ed3b2da5650270743604fe2cfa8a59a0f3f17ffc4d`  
		Last Modified: Tue, 05 May 2026 23:54:28 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888709ff5d4f866424bcf9b1d35f2ea63480060906d7d818e3d42c116b924f6d`  
		Last Modified: Wed, 06 May 2026 00:16:48 GMT  
		Size: 1.5 KB (1451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7243fe49b250626cd77d09f4130e10d65b0064b25f5cb25e68094078cfb79697`  
		Last Modified: Wed, 06 May 2026 00:16:51 GMT  
		Size: 57.8 MB (57752597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db8929eedcbffecd3940998a3844fc0f3bb5695c69c31dd5d4d63680dc57429`  
		Last Modified: Wed, 06 May 2026 00:16:53 GMT  
		Size: 140.2 MB (140235882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037cf2d08829da5fe05636aa2c289478b07bf260bda4c1cea3989ee8c64c39cc`  
		Last Modified: Wed, 06 May 2026 00:16:48 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:2ce6ab3fe60f268041f0030c8408684c3caea2513daad1fd94136ab0ca682203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7076080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786b2ce3c233279dd7f9f54ffc63b7428a9d5b7f695c0845f15996546f5d2cb9`

```dockerfile
```

-	Layers:
	-	`sha256:a491ea79ffa5c849df1b3ae92d70543399d379a6329e3f3bcab5d73085ec8804`  
		Last Modified: Wed, 06 May 2026 00:16:48 GMT  
		Size: 7.1 MB (7051557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d29e87963a010dbbe843d513d53a16e47cb11daeb06b5ab2aed9dd96ff6f26b9`  
		Last Modified: Wed, 06 May 2026 00:16:47 GMT  
		Size: 24.5 KB (24523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:81ac77aa5f2068a55c8701d93fdfd4cb5b50af42401879277069f2bae890b1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.5 MB (400531328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9f1be41bea147c010b2a86ab985492a2ec870a4b0e23bcfc8ca75783e9b576`
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
# Wed, 22 Apr 2026 18:16:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:22 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:22 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Wed, 22 Apr 2026 18:21:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:21:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:21:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:21:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:21:09 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:27:21 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:27:21 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:27:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:27:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:27:21 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:27:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:27:29 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:27:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:27:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:27:34 GMT
USER gradle
# Tue, 28 Apr 2026 23:27:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:27:35 GMT
USER root
```

-	Layers:
	-	`sha256:59053ba8a9d1e0e09d61b1f59967bb9ffc4505ef8eebe01b4c6808d9bce8b3a6`  
		Last Modified: Wed, 22 Apr 2026 06:16:12 GMT  
		Size: 34.4 MB (34437922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf755e7e06afeb41fd368fbfaae8e70f129c645bebe025cef69dbd8ac6c635`  
		Last Modified: Wed, 22 Apr 2026 18:17:40 GMT  
		Size: 37.8 MB (37849869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ecb6756b30a7262615576642351c0afca9014d35055c05de67416ea3a452fc`  
		Last Modified: Wed, 22 Apr 2026 18:22:36 GMT  
		Size: 147.1 MB (147104846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12fba956434599c3e0cb4c8f9d6771be2a0b953c72f376f8cc7838c0711d193c`  
		Last Modified: Wed, 22 Apr 2026 18:22:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32114eb95a536874e3cdeb894ce4281e626f3e41c48f78ddfe2ca8146fbee98`  
		Last Modified: Wed, 22 Apr 2026 18:22:26 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b67a8f7363895ae098dc0b21d70c232e1d28f6ce0a2c5266bb8375e3816bf`  
		Last Modified: Tue, 28 Apr 2026 23:28:09 GMT  
		Size: 1.6 KB (1591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5127f3d71ff1b1fa0f197ff775eb3b44e5da49d2262ca9e5cbc29c202646a0d`  
		Last Modified: Tue, 28 Apr 2026 23:28:12 GMT  
		Size: 40.9 MB (40898332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d022e450ccd5b9b33fe4054923f695f753df8701f2f2c4c31b96d55fa6ce08`  
		Last Modified: Tue, 28 Apr 2026 23:28:14 GMT  
		Size: 140.2 MB (140235942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8fb94b56480aa5582e68833bc054e56c93d85546a99664be124e770ab9df1d`  
		Last Modified: Tue, 28 Apr 2026 23:28:09 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:474d95b8368c73316722b78d0ed71fcef4ce42dcb3d82f6ef6f47322bf3d942f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9659a92d32c501201ab89e2b6a679a25cce06109ee5d4598670df381c92372f1`

```dockerfile
```

-	Layers:
	-	`sha256:4fd4ecfc9984668ffd8aab6071ff7b81a6766e3010fa456d97d488d93e6a06bb`  
		Last Modified: Tue, 28 Apr 2026 23:28:10 GMT  
		Size: 7.0 MB (7038352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:125603b80211fd95f65284cf527fbe3f7b5284e11c441a65c74ccf6d598f40d8`  
		Last Modified: Tue, 28 Apr 2026 23:28:09 GMT  
		Size: 24.4 KB (24449 bytes)  
		MIME: application/vnd.in-toto+json
