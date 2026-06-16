## `gradle:9-jdk26-ubi10`

```console
$ docker pull gradle@sha256:a503c4f0f444c37ac288182467a41fea98f29bc59a2f4ebf0fe4b787d4aff374
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

### `gradle:9-jdk26-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:4ce62d9fa76e3bd9faae694f405f08df166ce51673e52a93c7ffe68c113d0788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347318634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33df6446564028cd52541b1aa439de9e447193bc2e59369ca4668eb397ebb48f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 07:46:40 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 15 Jun 2026 07:46:40 GMT
ENV container oci
# Mon, 15 Jun 2026 07:46:41 GMT
COPY dir:6795a8753f13601990edb5b5276cfe7486fb53104b262115fb35fe817c2adf3b in /      
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 07:46:41 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:014278f73576f2def6d5cfa868c2c290482e8fb486fcfb5b865bcdf04c8c034a in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:41 GMT
COPY file:014278f73576f2def6d5cfa868c2c290482e8fb486fcfb5b865bcdf04c8c034a in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:41 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="a079bd1cc91523a60704cf840463d737ba8b63de" "org.opencontainers.image.revision"="a079bd1cc91523a60704cf840463d737ba8b63de" "build-date"="2026-06-15T07:46:21Z" "org.opencontainers.image.created"="2026-06-15T07:46:21Z" "release"="1781509346"org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de,org.opencontainers.image.created=2026-06-15T07:46:21Z
# Mon, 15 Jun 2026 23:14:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:14:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:14:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:12 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 15 Jun 2026 23:14:52 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:14:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:14:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:14:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:14:53 GMT
CMD ["jshell"]
# Mon, 15 Jun 2026 23:33:32 GMT
CMD ["gradle"]
# Mon, 15 Jun 2026 23:33:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 15 Jun 2026 23:33:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 15 Jun 2026 23:33:32 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 15 Jun 2026 23:33:32 GMT
WORKDIR /home/gradle
# Mon, 15 Jun 2026 23:33:35 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 15 Jun 2026 23:33:35 GMT
ENV GRADLE_VERSION=9.5.1
# Mon, 15 Jun 2026 23:33:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Mon, 15 Jun 2026 23:33:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:33:37 GMT
USER gradle
# Mon, 15 Jun 2026 23:33:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 15 Jun 2026 23:33:38 GMT
USER root
```

-	Layers:
	-	`sha256:0166415a5628b463967ca89a95832b5ecafa81aeddaca2f8713bec6e36a3c9c0`  
		Last Modified: Mon, 15 Jun 2026 08:52:54 GMT  
		Size: 34.9 MB (34914006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b30c31013ea9f8710620f0bc12e145089f28ba4bf5e5f4c3a2d4979fdf3d08`  
		Last Modified: Mon, 15 Jun 2026 23:14:37 GMT  
		Size: 37.8 MB (37761292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0680b9ab35d43b354f85b2d0222b5c0eaaca71571d2340a44a9d503160949a8`  
		Last Modified: Mon, 15 Jun 2026 23:15:11 GMT  
		Size: 94.5 MB (94525438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b30f3b767a55e56e483da4cb7f63c75dc0bd859369a5994fbb176f5b64ec51`  
		Last Modified: Mon, 15 Jun 2026 23:15:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafd49a23b1acb3bd74493626cd40c692c8990baa19dec48d4aa77d35463c46b`  
		Last Modified: Mon, 15 Jun 2026 23:15:09 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f3e4c886126a0ad24ae1db9f4f5d3125f6841de58484b08f4fd8d579974f05`  
		Last Modified: Mon, 15 Jun 2026 23:33:56 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d8379a1f885f3c2feb91176eae54532e0cfbcd814676d4b7a0a6e9fb89cf0f`  
		Last Modified: Mon, 15 Jun 2026 23:33:58 GMT  
		Size: 39.9 MB (39851078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4d12ba7543c611c3fe8c8de42c6aad3d5f9dced36c7e93c53a12d52ea043b1`  
		Last Modified: Mon, 15 Jun 2026 23:33:59 GMT  
		Size: 140.2 MB (140236987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331894f507d8873bb27910b2b0d2f78af6d6e683508796776478aab858c09045`  
		Last Modified: Mon, 15 Jun 2026 23:33:56 GMT  
		Size: 25.6 KB (25616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:c08387d6d29507f2518d765221f338fe8f7381706e8499477f2112c995a80030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7066056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69eeea47e393119f20de10b1b7d41a99b82ae798adf9b102c73c99d91659376`

```dockerfile
```

-	Layers:
	-	`sha256:d3a962a454d1bf985f7a0c3611b189e7db3b3c3efd497ffcf3a539ba9084ec78`  
		Last Modified: Mon, 15 Jun 2026 23:33:56 GMT  
		Size: 7.0 MB (7041635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9e72616a64739aa96087b3651f8f83aecfc89b0e7a7317f6bf8ee2bea2d371d`  
		Last Modified: Mon, 15 Jun 2026 23:33:56 GMT  
		Size: 24.4 KB (24421 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cc84be3dcc882f51b45e39bc02fdc8d64cdaa2d206eacabf39b6584aac79af71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343805531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d0e63c859730de14a74095a3f91611b8f3a0c69e53fb5ed48b5ab0ac49a5c8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 07:49:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 07:49:49 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 15 Jun 2026 07:49:49 GMT
ENV container oci
# Mon, 15 Jun 2026 07:49:49 GMT
COPY dir:96cf4a952c323db93c5acbd83a80198d6d4c582c6075283779408766bc1f06a0 in /      
# Mon, 15 Jun 2026 07:49:49 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 07:49:50 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:d017e9e035ec2f71c8ca63bbb7b57216ba5aad41669dc424f097659ae0649922 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:49:50 GMT
COPY file:d017e9e035ec2f71c8ca63bbb7b57216ba5aad41669dc424f097659ae0649922 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:49:50 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="a079bd1cc91523a60704cf840463d737ba8b63de" "org.opencontainers.image.revision"="a079bd1cc91523a60704cf840463d737ba8b63de" "build-date"="2026-06-15T07:49:33Z" "org.opencontainers.image.created"="2026-06-15T07:49:33Z" "release"="1781509346"org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de,org.opencontainers.image.created=2026-06-15T07:49:33Z
# Mon, 15 Jun 2026 23:13:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:38 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 15 Jun 2026 23:14:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:14:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:14:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:14:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:14:12 GMT
CMD ["jshell"]
# Mon, 15 Jun 2026 23:25:24 GMT
CMD ["gradle"]
# Mon, 15 Jun 2026 23:25:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 15 Jun 2026 23:25:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 15 Jun 2026 23:25:24 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 15 Jun 2026 23:25:24 GMT
WORKDIR /home/gradle
# Mon, 15 Jun 2026 23:25:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 15 Jun 2026 23:25:27 GMT
ENV GRADLE_VERSION=9.5.1
# Mon, 15 Jun 2026 23:25:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Mon, 15 Jun 2026 23:25:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:25:30 GMT
USER gradle
# Mon, 15 Jun 2026 23:25:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 15 Jun 2026 23:25:30 GMT
USER root
```

-	Layers:
	-	`sha256:2181b76d100cfec8fecaf70c9c757671f616064b9f875b0fb509a7b6a6788ac5`  
		Last Modified: Mon, 15 Jun 2026 09:25:44 GMT  
		Size: 33.0 MB (33030316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b214265a8401e53ac4e6a7258c3746c2536e1125900c4467e7b5eacf844038`  
		Last Modified: Mon, 15 Jun 2026 23:13:55 GMT  
		Size: 37.7 MB (37686395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2d0d22ef338750a9d980e23844cac75bd50117acc1537fb9cbf1fe771db370`  
		Last Modified: Mon, 15 Jun 2026 23:14:32 GMT  
		Size: 93.5 MB (93505273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775610f6aab15e19a72a3f494bd195945294e2a38212ebb38be9ba58836d2cba`  
		Last Modified: Mon, 15 Jun 2026 23:14:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8369c2b08b9b0cdf65e7669ac0b1aa39d26096510325eeafda17232b59cca80`  
		Last Modified: Mon, 15 Jun 2026 23:14:29 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f0ebb891383d64c189d5d61db3f5eaf6b392f4892c1487b109045d18be0611`  
		Last Modified: Mon, 15 Jun 2026 23:25:49 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff895c9262a16bc58148251a3530d9eab415a240081192c7d7c0b0fac436a74`  
		Last Modified: Mon, 15 Jun 2026 23:25:51 GMT  
		Size: 39.3 MB (39313012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ebf749e1b1d3590914db549d7fe98e88cce093a0af42480a96730d0c1e19e4`  
		Last Modified: Mon, 15 Jun 2026 23:25:53 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388d0cc18b85f192220b1f3a92374eb74af71a06f0a7fba125593a60ee2bd10c`  
		Last Modified: Mon, 15 Jun 2026 23:25:49 GMT  
		Size: 29.3 KB (29334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:477bbc4805b608580bdf0995a3eec19b70d8b4442957565c308ffa6a5b2a9d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7064506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef904ad7ec27e826b3e99cb709e4bc0b28d88c04ec6a601c925f91518ceacf1c`

```dockerfile
```

-	Layers:
	-	`sha256:d639a5814e042d9d845fb98448893b412563c4e51c9fbfdeb92acd8e199b2d77`  
		Last Modified: Mon, 15 Jun 2026 23:25:49 GMT  
		Size: 7.0 MB (7039888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65346a749674c9e36d0f5a9d502838ab038754fa2a9c903787ae70b15d0ac4b`  
		Last Modified: Mon, 15 Jun 2026 23:25:49 GMT  
		Size: 24.6 KB (24618 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:a7e0596f3b3a2773401365224f521d40cc639ab066b828204e2f3711db7202f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.3 MB (354314645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddc869a0b0bb79b4e3c0122bbbd16a4e6dbc21677c010cec106c320fa32ff6b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 07:46:33 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 15 Jun 2026 07:46:33 GMT
ENV container oci
# Mon, 15 Jun 2026 07:46:34 GMT
COPY dir:83033203513f54fa7ad30157591855861b9bdeeadfcfaa7b39d928026e30a43e in /      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 07:46:34 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:947556a1605dd2da1e7f452e2373e0e1a5352a517c46fbfad7c39a76efb34831 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:34 GMT
COPY file:947556a1605dd2da1e7f452e2373e0e1a5352a517c46fbfad7c39a76efb34831 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:46:34 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="a079bd1cc91523a60704cf840463d737ba8b63de" "org.opencontainers.image.revision"="a079bd1cc91523a60704cf840463d737ba8b63de" "build-date"="2026-06-15T07:46:22Z" "org.opencontainers.image.created"="2026-06-15T07:46:22Z" "release"="1781509346"org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de,org.opencontainers.image.created=2026-06-15T07:46:22Z
# Mon, 15 Jun 2026 23:14:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:14:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:14:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:23 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 15 Jun 2026 23:23:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:23:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:23:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:23:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:23:38 GMT
CMD ["jshell"]
# Tue, 16 Jun 2026 00:03:24 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 00:03:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 00:03:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 00:03:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 00:03:24 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 00:03:41 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 16 Jun 2026 00:03:41 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 16 Jun 2026 00:03:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 16 Jun 2026 00:03:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 00:03:45 GMT
USER gradle
# Tue, 16 Jun 2026 00:03:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 00:03:48 GMT
USER root
```

-	Layers:
	-	`sha256:2228c93141e55e5881a02fe1a8f242a1e8a66f3a905f628abec2236bd3b86b02`  
		Last Modified: Mon, 15 Jun 2026 12:17:19 GMT  
		Size: 39.0 MB (39037515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db47c543a6c879ca8da9aa74d1ba869d99590c43dc077909f584eca08199b2a`  
		Last Modified: Mon, 15 Jun 2026 23:15:00 GMT  
		Size: 39.5 MB (39521864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e975d91de768528cdbac353292d6d59bad1bbd739aca104f3ca9c303d1fb61`  
		Last Modified: Mon, 15 Jun 2026 23:24:13 GMT  
		Size: 93.9 MB (93902393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afc2421ba2d2434433c57b9543ed0cb8742ab48f7f1d5964194b8db9eb4f2f2`  
		Last Modified: Mon, 15 Jun 2026 23:24:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17a84957f06835d7967d7ed02eb345469f069e118168db2f6c9d1247681556b`  
		Last Modified: Mon, 15 Jun 2026 23:24:10 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23885077d9de996f95851355162d2b216be2eccb809bad87a18ea2f8a736ef4c`  
		Last Modified: Tue, 16 Jun 2026 00:04:30 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c9a02d07420cc0fe5ca516ce54146023a67c6a4742003cd13a794483ff6641`  
		Last Modified: Tue, 16 Jun 2026 00:04:32 GMT  
		Size: 41.6 MB (41611288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2c1767bdc061e13d8cba3ef01f14f247615d9f31963e73d618aebd6bf654f1`  
		Last Modified: Tue, 16 Jun 2026 00:04:34 GMT  
		Size: 140.2 MB (140236990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19edbcc8c3754f05812bdc72bc6f0124a19869c126a00e07a63cf4d56cd906f`  
		Last Modified: Tue, 16 Jun 2026 00:04:30 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:ecdb05f654442dd532a25f19a8663d878de9cb2749f7855ebd92ac1eb009370d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7041482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3503295093aaeeeeadc513de4716563f44053a4d4be0809235c5ce12fefd003`

```dockerfile
```

-	Layers:
	-	`sha256:7dc471cd062b96f9ad0bbf6c3d6f0a4e7278029ba03a2feb792fe150ca82b842`  
		Last Modified: Tue, 16 Jun 2026 00:04:30 GMT  
		Size: 7.0 MB (7016989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4116f876eb4a3eeb9806a32e1765c8de84c4359549802534405579281a76142d`  
		Last Modified: Tue, 16 Jun 2026 00:04:30 GMT  
		Size: 24.5 KB (24493 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:ec674d30c90094bc34daa030290be2a846acb72fcb567e0b54a6d71bbd2d3dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.6 MB (345648800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45348f37b027326ff1c25cc4cf1cf87d46f1ab66fb14cd815bf546274dec0fac`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 07:55:07 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 15 Jun 2026 07:55:07 GMT
ENV container oci
# Mon, 15 Jun 2026 07:55:08 GMT
COPY dir:68c536b999ac54f0dfd3ea639a66f6d8b8e801e02f0906bfd4f0f3d49b80c8ef in /      
# Mon, 15 Jun 2026 07:55:08 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 07:55:08 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 07:55:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 07:55:08 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 07:55:08 GMT
COPY file:5997c8f26aac6fe4f78de1f6a3bc547b61b6f2f31d9024efa02f0dafe9cbb6f0 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:55:08 GMT
COPY file:5997c8f26aac6fe4f78de1f6a3bc547b61b6f2f31d9024efa02f0dafe9cbb6f0 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 07:55:08 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="a079bd1cc91523a60704cf840463d737ba8b63de" "org.opencontainers.image.revision"="a079bd1cc91523a60704cf840463d737ba8b63de" "build-date"="2026-06-15T07:54:24Z" "org.opencontainers.image.created"="2026-06-15T07:54:24Z" "release"="1781509346"org.opencontainers.image.revision=a079bd1cc91523a60704cf840463d737ba8b63de,org.opencontainers.image.created=2026-06-15T07:54:24Z
# Mon, 15 Jun 2026 23:12:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:12:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:12:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:12:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:12:41 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Mon, 15 Jun 2026 23:15:30 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:15:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:15:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:15:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:15:32 GMT
CMD ["jshell"]
# Tue, 16 Jun 2026 00:00:26 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 00:00:26 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 00:00:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 00:00:26 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 00:00:26 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 00:00:39 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 16 Jun 2026 00:00:39 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 16 Jun 2026 00:00:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 16 Jun 2026 00:00:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 00:00:43 GMT
USER gradle
# Tue, 16 Jun 2026 00:00:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 00:00:44 GMT
USER root
```

-	Layers:
	-	`sha256:6b559f707189dd761fe2428430b64fd3ce2ba067087434dff94472da1719acfe`  
		Last Modified: Mon, 15 Jun 2026 12:17:11 GMT  
		Size: 34.8 MB (34761540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9110e30c90acabaeecd57254cf2d8b9ccedf77c5f6267a4119fd623d01837a9e`  
		Last Modified: Mon, 15 Jun 2026 23:13:18 GMT  
		Size: 38.1 MB (38140021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c20120060f8833bdd1491447c6b4c236d6b33dcce33a0399257b0939335fac6`  
		Last Modified: Mon, 15 Jun 2026 23:16:01 GMT  
		Size: 90.5 MB (90537368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3bc68dff56a91ded0265c53a8782fb0223f2e875b33521ac699794ee2657cb`  
		Last Modified: Mon, 15 Jun 2026 23:15:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6439e2dfd6a5771b7006f02db6914a9b7d8a0c32e2f8450666ef0d8aadaaccd`  
		Last Modified: Mon, 15 Jun 2026 23:16:00 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62db9c3914aa016aa5ec931dc4baf485a4aeccd40b9f8287adcd02303dd58d6`  
		Last Modified: Tue, 16 Jun 2026 00:01:17 GMT  
		Size: 1.6 KB (1589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9a008b12dbf407d3d396c17d5418cc4bc1d802e839c1cdd9c2661905eb9da0`  
		Last Modified: Tue, 16 Jun 2026 00:01:18 GMT  
		Size: 42.0 MB (41968284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21337f55916712b7f756c3d2cffb3cebef7a6e8a4bc336df727221c414c9b7e`  
		Last Modified: Tue, 16 Jun 2026 00:01:20 GMT  
		Size: 140.2 MB (140236989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5873e6156fdb5f2bb8fb6f34c391efb0a5c9cc272ead24e141516724756c6b52`  
		Last Modified: Tue, 16 Jun 2026 00:01:17 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:0274527f5f759f9bb31ce3e749a9ad279b32d66c449f38d391915eb3ea2eeb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7031887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab027f59c2e301c3c400cd61151c4214e4d11b6d768a9fece59ccf456f75fd4e`

```dockerfile
```

-	Layers:
	-	`sha256:951dedf7f8427ec2af9fae10d851a056e5aa4ec44a6e532ba74e9a320fe013f5`  
		Last Modified: Tue, 16 Jun 2026 00:01:17 GMT  
		Size: 7.0 MB (7007468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2129a4ff878a6e969c66b8574a8287c8c8f83b22e86e96e6390a31d40e65f679`  
		Last Modified: Tue, 16 Jun 2026 00:01:16 GMT  
		Size: 24.4 KB (24419 bytes)  
		MIME: application/vnd.in-toto+json
