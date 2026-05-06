## `gradle:jdk25-ubi10`

```console
$ docker pull gradle@sha256:49a167cb8a5b3079244bb6edeec8f7868e2ec897943e05ff3220f2ad6205a002
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

### `gradle:jdk25-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:ad484bf9715c1a435d6a1e15ac6d6688984b3f95c8823d623182e6538c9e6d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.9 MB (344944573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16742c998606ad441e6286828d1fcbb2f126361b991b99fd721387341abda7e`
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
# Tue, 05 May 2026 23:08:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:48 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 05 May 2026 23:08:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:55 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:11:03 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:11:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:11:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:11:03 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:11:03 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:11:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:11:08 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 00:11:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Wed, 06 May 2026 00:11:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:11:10 GMT
USER gradle
# Wed, 06 May 2026 00:11:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 06 May 2026 00:11:11 GMT
USER root
```

-	Layers:
	-	`sha256:6c2848906904fdb30be3302af6950faf3bb49f8acf1fe7da43266ab561f76092`  
		Last Modified: Mon, 04 May 2026 03:13:50 GMT  
		Size: 34.6 MB (34648199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84ecd8549c867718c9bf17705ebeceb28962c44b107e0a591c05d47a1e7939c`  
		Last Modified: Tue, 05 May 2026 23:09:12 GMT  
		Size: 22.0 MB (22037162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff3e421b849f046c42423414596ab97898091b2d533429244323448f89c59ea`  
		Last Modified: Tue, 05 May 2026 23:09:14 GMT  
		Size: 92.6 MB (92579347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3ff0f9aeab08ab5f03745c30b701ff7bfcbe6a30dba32e9a9d4591305955f5`  
		Last Modified: Tue, 05 May 2026 23:09:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00867497883efeb83d0e1e322c7b569c4f729644503a69c03b3a00b955dba057`  
		Last Modified: Tue, 05 May 2026 23:09:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7795ed6fd3b7f989ec22606387003d752669243fb4b10fe9de27de97a698fa7`  
		Last Modified: Wed, 06 May 2026 00:11:29 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce3400d6d8f8db3257681b248dee97b43c45c7d717ca40ecd683d027a2e7f20`  
		Last Modified: Wed, 06 May 2026 00:11:32 GMT  
		Size: 55.4 MB (55414426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ff367883881e661977a98b0273aee2b664aeb47be0909fb754f66385fb36f1`  
		Last Modified: Wed, 06 May 2026 00:11:34 GMT  
		Size: 140.2 MB (140235927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1371d34569b183589c1ab84792bcc8f8c9472fb4063fac20a229e6f77fd4fe6e`  
		Last Modified: Wed, 06 May 2026 00:11:29 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:c1656f67795a6ad9fba8ceb8161938ff2d4f57260dc415955cc6052fc1a3aa4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7051905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3593611e30bef67b9db48f0e1d136f361035a455895c66f79a589c217305656f`

```dockerfile
```

-	Layers:
	-	`sha256:8b18e1316e7e82bccb82665b565187ec2d9534cb4450fccac98f737ac2e465f6`  
		Last Modified: Wed, 06 May 2026 00:11:29 GMT  
		Size: 7.0 MB (7026896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0786bd42e71741dbca3cbb2bb2bcd5a88c0514b13e4117dcc09f46cf77e983`  
		Last Modified: Wed, 06 May 2026 00:11:29 GMT  
		Size: 25.0 KB (25009 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7845b571c9fde4fc8cd548ddbfcac1e27bcb62389636413c4e10f6ffd4e9e1b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341413043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51861d5f295ecd6fa18be65b13503dbc007f063d6c1daef372e8db6c7c9de220`
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
# Tue, 05 May 2026 23:07:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:07:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:07:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:07:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:07:48 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 05 May 2026 23:08:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:32 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:11:25 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:11:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:11:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:11:25 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:11:25 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:11:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:11:31 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 00:11:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Wed, 06 May 2026 00:11:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:11:34 GMT
USER gradle
# Wed, 06 May 2026 00:11:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 06 May 2026 00:11:34 GMT
USER root
```

-	Layers:
	-	`sha256:908809553a77ac560aff532a902be43c3a99a0dcb4f759158a75984cb82c4b9d`  
		Last Modified: Mon, 04 May 2026 06:16:39 GMT  
		Size: 32.7 MB (32711611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d709fca6869e22fad5c9b0dbb700e99686d54ee17d198ca1f03be45dd35173`  
		Last Modified: Tue, 05 May 2026 23:08:15 GMT  
		Size: 22.3 MB (22301544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb49282fa42a22abc9f416e6a2bc18ea0b805160b10bc9fdceb8c77b0dda910e`  
		Last Modified: Tue, 05 May 2026 23:08:50 GMT  
		Size: 91.5 MB (91548891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75814aebbbdd128d7c010b4d74e33102a23d6065e9b014e251b00b1151e9fa18`  
		Last Modified: Tue, 05 May 2026 23:08:47 GMT  
		Size: 132.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23b5e9733f87740fb1cc3559283b6a2f665eeec5ecb73888d19d934f78b16ed`  
		Last Modified: Tue, 05 May 2026 23:08:47 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5277864879423f665d496b5ea0b3646a2713b49a60ae22f6def258001c3751`  
		Last Modified: Wed, 06 May 2026 00:11:54 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b671606d4066d5fdcea627c66ae94232eee577e186c87b8a08dc8c750200cd1`  
		Last Modified: Wed, 06 May 2026 00:11:57 GMT  
		Size: 54.6 MB (54581817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728c0af9d1aedcacc5976147cdbade813e959433b99d71ef0c7e20e3ad850167`  
		Last Modified: Wed, 06 May 2026 00:11:59 GMT  
		Size: 140.2 MB (140235942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaa992446fe5d5a670e244dcee14d160e3229f413944a6fc9219b33f7065c17`  
		Last Modified: Wed, 06 May 2026 00:11:55 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:cef2b10a9eb6b44e548227ab4673e937d7d6e9d7b8f4bb70cf718b37cb1571e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7050403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07e55f27d940d3a79b36f95415d2d4207303cd6d35b0073cd0843dfa0fd7d99`

```dockerfile
```

-	Layers:
	-	`sha256:39b84c9aee55056deecdc93fb16e5f62a258bb3090d663bbb7ff9437ce6d4bd6`  
		Last Modified: Wed, 06 May 2026 00:11:55 GMT  
		Size: 7.0 MB (7025173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0cf1c79baec64c9609e66f9d7e43ee580a99ea32ace15cead98c12cfb4f0cd8`  
		Last Modified: Wed, 06 May 2026 00:11:54 GMT  
		Size: 25.2 KB (25230 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:ae682cb76053626e1b3e8504353099ee7c2c4324774845e706774ed746afee0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351985229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e443afedf941db5993cd5c917c9f2c46f22d7561b7706e2c3ec110a68f5eec3`
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
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 05 May 2026 23:55:50 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:55:54 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:55:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:55:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:55:55 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:15:15 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:15:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:15:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:15:15 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:15:15 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:15:54 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:15:54 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 00:15:54 GMT
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
	-	`sha256:cb0722df8d5a63086214514e2b2ed963158efb80532f575ca2d8e8c8a3e59246`  
		Last Modified: Tue, 05 May 2026 23:56:33 GMT  
		Size: 91.9 MB (91912860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c25ae0c95aa98c3613a032a1d8d46a840a3df691c433fc588b12d22ca344c6`  
		Last Modified: Tue, 05 May 2026 23:56:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66154d20559b24f0a2ae006c737bb54cf6e4b0a8dfd6eacd560f7f4bbfae7169`  
		Last Modified: Tue, 05 May 2026 23:56:31 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646e76fab32ead354b36ee49f9732b57cc51abef32948762bc959b94adcab529`  
		Last Modified: Wed, 06 May 2026 00:16:47 GMT  
		Size: 1.5 KB (1454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e512ce458e4f2e1718ee7f696c5f4290962aa5450588f9baea7da34995312586`  
		Last Modified: Wed, 06 May 2026 00:16:50 GMT  
		Size: 57.8 MB (57752545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bab68d3509523e6927a71e75fb2332647f78e97536bf57ef43c495ef429660`  
		Last Modified: Wed, 06 May 2026 00:16:53 GMT  
		Size: 140.2 MB (140235941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9ae1ff7411a45a60658ae80d670772d065bd2f16373dd383673b1ef120b057`  
		Last Modified: Wed, 06 May 2026 00:16:47 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:a27ea4e06985b2812724df146f1b62f00d665ad636578de820d6a9bede0b5498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7026731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0013ac63c9e5e4ac8f845ffd5e476461a129ce6497cc6c9b65b29acab77adc`

```dockerfile
```

-	Layers:
	-	`sha256:f688287067c2a735c0eac7237bfed87de97f3f364781bb19c35096da1fcd2bed`  
		Last Modified: Wed, 06 May 2026 00:16:48 GMT  
		Size: 7.0 MB (7001638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246aceb65588ce62e6835cbfc4496d1dc19ee0d3052ad6b40bb40c85ace1ab9d`  
		Last Modified: Wed, 06 May 2026 00:16:47 GMT  
		Size: 25.1 KB (25093 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:e42a112dcc6157ab57f33ef90becde23f8e7f2dfd7788480d51b5c80e95534c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343068149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aefd1e5f2034bdb1e66c43faea5e1991a35f999698e3d5ab537dfc5a621524`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:46:56 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:46:56 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:46:56 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:46:56 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 04 May 2026 01:46:56 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:46:56 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 04 May 2026 01:46:56 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:46:56 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 04 May 2026 01:46:56 GMT
ENV container oci
# Mon, 04 May 2026 01:46:56 GMT
COPY dir:cacbd48510196fa765f2d5bccb8b2b0023c608fcbd86154b6fe34e775acd2483 in /      
# Mon, 04 May 2026 01:46:56 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:46:56 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:46:56 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:6983ce2775fc6ec74b2d7c54d91fce16f639c26d824bf41c774ba5d5ae4037e9 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:46:57 GMT
COPY file:6983ce2775fc6ec74b2d7c54d91fce16f639c26d824bf41c774ba5d5ae4037e9 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:46:57 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2c4967ab62628fff803457df7635994ca0e85fbc" "org.opencontainers.image.revision"="2c4967ab62628fff803457df7635994ca0e85fbc" "build-date"="2026-05-04T01:46:14Z" "org.opencontainers.image.created"="2026-05-04T01:46:14Z" "release"="1777858393"org.opencontainers.image.revision=2c4967ab62628fff803457df7635994ca0e85fbc,org.opencontainers.image.created=2026-05-04T01:46:14Z
# Wed, 06 May 2026 00:08:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 May 2026 00:08:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 00:08:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 May 2026 00:08:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 06 May 2026 00:08:32 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Wed, 06 May 2026 00:13:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3e4287cb98870ba824ed698854bdc27cff984254caf66dd12cc291e7bfdde26b';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_aarch64_linux_hotspot_25.0.3_9.tar.gz';          ;;        ppc64le)          ESUM='72b0fbb201716ca465ab704ec0fb12971abab3fdde5ae8d03b125a273522cf05';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_ppc64le_linux_hotspot_25.0.3_9.tar.gz';          ;;        s390x)          ESUM='24b497d10acb6ee706ca30e1c8a929785c250cad54c5c12f1f8f93c3c06a53f7';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_s390x_linux_hotspot_25.0.3_9.tar.gz';          ;;        x86_64)          ESUM='69264a7a211bf5029830d07bc3370f879769d62ebc5b5488e90c9343a2da0e1f';          BINARY_URL='https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.3%2B9/OpenJDK25U-jdk_x64_linux_hotspot_25.0.3_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 06 May 2026 00:13:40 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 06 May 2026 00:13:40 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 06 May 2026 00:13:40 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 00:13:40 GMT
CMD ["jshell"]
# Wed, 06 May 2026 01:10:19 GMT
CMD ["gradle"]
# Wed, 06 May 2026 01:10:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 01:10:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 01:10:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 01:10:19 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 01:10:28 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 01:10:28 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 01:10:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Wed, 06 May 2026 01:10:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 01:10:32 GMT
USER gradle
# Wed, 06 May 2026 01:10:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 06 May 2026 01:10:32 GMT
USER root
```

-	Layers:
	-	`sha256:e434a7e4a8db18a3b2f706d5c1b2a02cfe20f46083a805f7dcf9e2e92903aa2e`  
		Last Modified: Mon, 04 May 2026 06:16:45 GMT  
		Size: 34.4 MB (34430001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06a4a5291aa3dc425a53819ce535f60012137e7f9e2faeddeef31090147f8e5`  
		Last Modified: Wed, 06 May 2026 00:09:06 GMT  
		Size: 22.4 MB (22365064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b39f0e16b485cfe371e537cd9b3dbb26a9122da67f161c5ee88c8b28ff5fc5`  
		Last Modified: Wed, 06 May 2026 00:14:13 GMT  
		Size: 88.4 MB (88421727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab42ce92191b67015ca51dce20b21739a41eda8bbb01fa8621bed6d0c0fee955`  
		Last Modified: Wed, 06 May 2026 00:14:11 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7455d4edc4cdaa8802c19ba582909fef1095de22b0efbd4460546f96ccf7348e`  
		Last Modified: Wed, 06 May 2026 00:14:11 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d3059dccb10afa01142522dc7f5ac8c1b7e112dc99555e6984b7868e858e5b`  
		Last Modified: Wed, 06 May 2026 01:11:09 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc6c7292ff21cb0d153e5b179710d709aba0ef9e0100f77ef4b7484b3866245`  
		Last Modified: Wed, 06 May 2026 01:11:11 GMT  
		Size: 57.6 MB (57611179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb49ac59c8c5b0a4b58ba429da736ce930b2d84b906f9e78cc88026ee2c3c48`  
		Last Modified: Wed, 06 May 2026 01:11:14 GMT  
		Size: 140.2 MB (140235902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ccca388a04093f238380364cb9a828485bc96e9c0cdb9e8258b611aacf2591`  
		Last Modified: Wed, 06 May 2026 01:11:09 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:2e89b3a3933ff68aada9ef5dca1f7d144c8602fb7b54256c82cdea935d08e0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7017112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b665f7f079b473c4c41b382117cbb7306eb62a26cb63c0e92c9d500f4df4e90`

```dockerfile
```

-	Layers:
	-	`sha256:1395cd7135cb8ea6dc21fdb38f3f576edf0715231d525cd11ce0029ce05e82e8`  
		Last Modified: Wed, 06 May 2026 01:11:09 GMT  
		Size: 7.0 MB (6992105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583f8e9630801d5f39079d76d49926abf89b4cd2960d6a157f32566a1f341f79`  
		Last Modified: Wed, 06 May 2026 01:11:09 GMT  
		Size: 25.0 KB (25007 bytes)  
		MIME: application/vnd.in-toto+json
