## `gradle:9-jdk26-ubi`

```console
$ docker pull gradle@sha256:2cdb52b73d6e6bdddc68ec406a27ea87447d12cb445f358f9a5bf739b8d4e16e
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

### `gradle:9-jdk26-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:fa97684f253f98bef383f5f644e10697f95e26246743a0d84d8d116456726b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347286015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3987660dd0c014b5101e9d4fb21fd5198a767a7384510e8ae0727f8ebf4fa2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 27 May 2026 06:12:12 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:12:12 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:12:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:12:12 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:12:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:12:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:12:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:12:12 GMT
ENV container oci
# Wed, 27 May 2026 06:12:12 GMT
COPY dir:8cc023cf96d9d3899063545e0c3b25ee410727bc8ef5903cc1b3e3e22d98dc1f in /      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:12:13 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:12:13 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:919ce0635818e127299907aac3d5ec8b04328702d69e0d804c99d87a631c2e20 in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:919ce0635818e127299907aac3d5ec8b04328702d69e0d804c99d87a631c2e20 in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:12:13 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:11:58Z" "org.opencontainers.image.created"="2026-05-27T06:11:58Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:11:58Z
# Wed, 27 May 2026 22:37:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:37:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:37:01 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:37:01 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:37:01 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Wed, 27 May 2026 22:37:33 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:37:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:37:34 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:37:34 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:37:34 GMT
CMD ["jshell"]
# Wed, 27 May 2026 23:11:05 GMT
CMD ["gradle"]
# Wed, 27 May 2026 23:11:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 23:11:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 23:11:05 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 23:11:05 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 23:11:09 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 23:11:09 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 23:11:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 23:11:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 23:11:12 GMT
USER gradle
# Wed, 27 May 2026 23:11:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 23:11:12 GMT
USER root
```

-	Layers:
	-	`sha256:8b457fb1b26320aa35da6d429ea0efa5a81d9f904a24a8d0a4e1a1efcfd0e7b8`  
		Last Modified: Wed, 27 May 2026 07:33:17 GMT  
		Size: 34.9 MB (34902395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e615f95d10dc6a9d46d4cb540c3457156c62a1c39a3538609ecb7e5ef1174be`  
		Last Modified: Wed, 27 May 2026 22:37:19 GMT  
		Size: 37.7 MB (37749648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f45eac5ac2ae73cfb97e30e224a60ef92943b4046a7a96bf0bf80071c02721f`  
		Last Modified: Wed, 27 May 2026 22:37:53 GMT  
		Size: 94.5 MB (94525405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8984b21e43a57d36abf54a0591cbad1a4cde6f8ced71ada108372530e8b4c659`  
		Last Modified: Wed, 27 May 2026 22:37:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361619a75804e5af08725ea3a63ba3ecc9bd58a188934d34072c1c64ec6894bc`  
		Last Modified: Wed, 27 May 2026 22:37:51 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b51c17fa3e9d65599e861d8e0bb7006d6696d0d4c3aca0437eb4d037f1eecb7`  
		Last Modified: Wed, 27 May 2026 23:11:31 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d384208b811205147051d70f8ac7e374567a0eb19a17a52f748ad8d9e56430`  
		Last Modified: Wed, 27 May 2026 23:11:33 GMT  
		Size: 39.8 MB (39841752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bcd01cdc49c28442f993091e9992eb31a3f90aebc72fcfbf729acffcfaf818`  
		Last Modified: Wed, 27 May 2026 23:11:35 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a484c15294db111a254aa6ef688587d77c57e2355e66359fcecc16130d533b`  
		Last Modified: Wed, 27 May 2026 23:11:31 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:af9ae409acc9983c0ab597abf2a94a4d2436675247171a5dfeb81ca14337a035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7066039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502a020e5decc18de62878514fddfa3395a364e7a480b8fd8a567b81245d47bf`

```dockerfile
```

-	Layers:
	-	`sha256:8177024d962d86cb25f90270c1b9f6b25570990cd143e75368a3ef921349b0be`  
		Last Modified: Wed, 27 May 2026 23:11:31 GMT  
		Size: 7.0 MB (7041619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee8f9180d0f20515f591a271cc5ac2dfba19281b2b8d0328ff753cfdd5074a7e`  
		Last Modified: Wed, 27 May 2026 23:11:30 GMT  
		Size: 24.4 KB (24420 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:25ba8104ce086f4e63a9db892a6971316fba1c24008ff94169cb9dd8a5e04b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343816653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a86143b165daed7bb7c969c685f82f2e375a5082d640bf11834911aafff53db`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 27 May 2026 06:14:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:14:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:14:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:14:32 GMT
ENV container oci
# Wed, 27 May 2026 06:14:33 GMT
COPY dir:144798cc4c14efe6d25c10c7a6f149af1045784afd86a94e99d04f534f9bbb05 in /      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:14:33 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:14:17Z" "org.opencontainers.image.created"="2026-05-27T06:14:17Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:14:17Z
# Wed, 27 May 2026 22:37:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:37:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:37:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:37:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:37:32 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Wed, 27 May 2026 22:38:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:38:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:38:06 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:38:06 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:38:06 GMT
CMD ["jshell"]
# Wed, 27 May 2026 23:10:57 GMT
CMD ["gradle"]
# Wed, 27 May 2026 23:10:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 23:10:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 23:10:57 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 23:10:57 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 23:11:00 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 23:11:00 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 23:11:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 23:11:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 23:11:03 GMT
USER gradle
# Wed, 27 May 2026 23:11:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 23:11:04 GMT
USER root
```

-	Layers:
	-	`sha256:94a14999202bc800f78441edfa1b48a3f6b5a799655652a41a4ef92004acb9c3`  
		Last Modified: Wed, 27 May 2026 07:33:15 GMT  
		Size: 33.1 MB (33062079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f12871f3dab5787849357117edfa21e2e36696b6af192a3b7cf09171e8d1ab`  
		Last Modified: Wed, 27 May 2026 22:37:50 GMT  
		Size: 37.7 MB (37681296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f6455a3bd0a899f1aaf7ff170b52f77a157488718b887d3c4f38f2e014a819`  
		Last Modified: Wed, 27 May 2026 22:38:25 GMT  
		Size: 93.5 MB (93505274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ff1ec15834113982c9157a21cfa55b874c4b7c756e834b0204d344599efa10`  
		Last Modified: Wed, 27 May 2026 22:38:23 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712d00dc7a6c5b5435d598697fd2f536bab4923f5f8af81e19a8f008301fe777`  
		Last Modified: Wed, 27 May 2026 22:38:18 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdc331afcb45b90147af4e186c9dfe3d7f0cb96c1e416f08f6c1bb6ad75e41f`  
		Last Modified: Wed, 27 May 2026 23:11:22 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1fec3294b24e37cef54c6469f09b8a3b46145c5b0c72f4a73549a7ad19f8cf`  
		Last Modified: Wed, 27 May 2026 23:11:24 GMT  
		Size: 39.3 MB (39297464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92159ed1db9a4f28c7a56b32f5838f7be3f5e01a61a107f4b06cd3aeef21502`  
		Last Modified: Wed, 27 May 2026 23:11:26 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de42dc9a1ed5b44bd128d6de55a279cfe16e7640d97a198d029cd49df34328c`  
		Last Modified: Wed, 27 May 2026 23:11:22 GMT  
		Size: 29.3 KB (29338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:ec1d818fa2be86dff7165cbf9860dcce44f8394bc521703f981a74daf7bda75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7064489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ca9bf0146781c537c4f26e30778b3d0943f651f9d3961dc4d29972ad7ff3c6`

```dockerfile
```

-	Layers:
	-	`sha256:cf9631503a26a066127abdbdb7754f092a2ab2b10f18aaad9d631c1a8d59caea`  
		Last Modified: Wed, 27 May 2026 23:11:22 GMT  
		Size: 7.0 MB (7039872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2668b67b63cd39a4d176eb72769d7ba77ff82ddc0351ef55acfd14db959a0e9f`  
		Last Modified: Wed, 27 May 2026 23:11:22 GMT  
		Size: 24.6 KB (24617 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:6c0af77ce2952b2e43c11aa1c990c95a34bc2af62234d92d12426a3780caa7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.3 MB (354269944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66333554c7bb14c952a063c3d1cfe59cf9dcd1f9bf7e3c433f47f739e6910184`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 27 May 2026 06:14:57 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:14:57 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:14:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:14:58 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:14:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:14:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:14:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:14:59 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:14:59 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:15:00 GMT
ENV container oci
# Wed, 27 May 2026 06:15:05 GMT
COPY dir:3c79ef63a7976ed53bc357ee61420f17b1c4d01f16daa9a157b46e996d5ae20c in /      
# Wed, 27 May 2026 06:15:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:15:06 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:15:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:15:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:15:08 GMT
COPY file:5604aea5cf04212fca8939538465f845888885b3e8d5cba8ef672e5a589974b7 in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:15:10 GMT
COPY file:5604aea5cf04212fca8939538465f845888885b3e8d5cba8ef672e5a589974b7 in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:15:11 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:13:56Z" "org.opencontainers.image.created"="2026-05-27T06:13:56Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:13:56Z
# Wed, 27 May 2026 22:50:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:50:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:50:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:50:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:50:47 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Wed, 27 May 2026 22:55:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:55:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:55:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:55:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:55:52 GMT
CMD ["jshell"]
# Wed, 27 May 2026 23:10:59 GMT
CMD ["gradle"]
# Wed, 27 May 2026 23:10:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 23:10:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 23:10:59 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 23:10:59 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 23:11:18 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 23:11:18 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 23:11:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 23:11:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 23:11:23 GMT
USER gradle
# Wed, 27 May 2026 23:11:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 23:11:25 GMT
USER root
```

-	Layers:
	-	`sha256:d339a2f2276a8d859309603363be4a2e3264f8a5a443e066c45ef5518856d381`  
		Last Modified: Wed, 27 May 2026 10:57:44 GMT  
		Size: 39.0 MB (39023856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58939e04772041c6139b9c72eb21d342c8fe4b6f1a4fe1a247ee089431c487cc`  
		Last Modified: Wed, 27 May 2026 22:51:27 GMT  
		Size: 39.5 MB (39503510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334c039c4ef203216aff9eeb9b0e3dd03e813d58d5bdd27b73a0f513b9f1c39`  
		Last Modified: Wed, 27 May 2026 22:56:29 GMT  
		Size: 93.9 MB (93902368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d730f8cd9d0fe9a5c7bfd9a4d5b1af92cf41e93b43711f896894d1b3ff2e98`  
		Last Modified: Wed, 27 May 2026 22:56:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a9dfbabc688fd626bd1cea5022189b1a3314a805f36cafa49a58236fc09bd2`  
		Last Modified: Wed, 27 May 2026 22:56:26 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adb7305a3a4f1d7aedec3353d0651a4a4ee0c3fcf9f575ad8de5187c0b4c683`  
		Last Modified: Wed, 27 May 2026 23:12:02 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967849ac84a6dcad0179f58d529901b7ff3a7da319948980fcce389589750685`  
		Last Modified: Wed, 27 May 2026 23:12:04 GMT  
		Size: 41.6 MB (41598624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f53493d43470dab833ee9f6dde87fa0ac0cd84e36a7027c14ad07ebcb41610`  
		Last Modified: Wed, 27 May 2026 23:12:07 GMT  
		Size: 140.2 MB (140236983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537b2f51903b0b12d1d5e690d67ee8c9ba5a693d3c836fa691bb88eb2a3f6118`  
		Last Modified: Wed, 27 May 2026 23:12:02 GMT  
		Size: 382.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:4e417ae957b5cff9844f0426517e975c96afd41fb3306605cbfc2ba92e0c4522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7041466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee015d20da45befde63f65285699da6feb01b0f60b0a656677426bf9b781b5d0`

```dockerfile
```

-	Layers:
	-	`sha256:d6840f9a9f63cd2e1165176af48ea5736ac9faeb29f5f58c72a59d125e6f17b9`  
		Last Modified: Wed, 27 May 2026 23:12:03 GMT  
		Size: 7.0 MB (7016973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0387c73b7bfcaadbcfacdc26c9381a1d43a99c0b5f4e94f39db62c5eaf2b1e77`  
		Last Modified: Wed, 27 May 2026 23:12:02 GMT  
		Size: 24.5 KB (24493 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:0d12f5d3c9ee839c44a6dbda478fae09598c353aef9d64258b9f57c8d66f2add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.5 MB (345536705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ee4230e7237a3137d737a63c4bf3634fec99e69a9aa09f3bacfd58c0a04645`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 27 May 2026 06:37:00 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:37:00 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:37:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:37:00 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:37:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:37:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:37:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:37:00 GMT
ENV container oci
# Wed, 27 May 2026 06:37:01 GMT
COPY dir:24d1f0c37ae2ecf8290e1663d221246314d1b68d602e33735e6d32665445372e in /      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:37:01 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:37:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:4188614bc7118984387709b86ec90ee5a895ba0f9b561a8cf875fcae15cc3f1f in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:4188614bc7118984387709b86ec90ee5a895ba0f9b561a8cf875fcae15cc3f1f in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:37:01 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:36:19Z" "org.opencontainers.image.created"="2026-05-27T06:36:19Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:36:19Z
# Wed, 27 May 2026 22:39:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:39:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:39:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:39:29 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:39:29 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Wed, 27 May 2026 22:40:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:41:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:41:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:41:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:41:00 GMT
CMD ["jshell"]
# Wed, 27 May 2026 23:09:45 GMT
CMD ["gradle"]
# Wed, 27 May 2026 23:09:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 23:09:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 23:09:45 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 23:09:45 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 23:09:51 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 23:09:51 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 23:09:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 23:09:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 23:09:56 GMT
USER gradle
# Wed, 27 May 2026 23:09:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 23:09:56 GMT
USER root
```

-	Layers:
	-	`sha256:5e0d999553a87b2b92e291dab9ef17c167202f1dbb15b260d71e176269309f5d`  
		Last Modified: Wed, 27 May 2026 10:57:27 GMT  
		Size: 34.7 MB (34680084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3ffe2d813e29ceb25c4df1d57a3290b5f3ee7533776116093016276701fffb`  
		Last Modified: Wed, 27 May 2026 22:39:55 GMT  
		Size: 38.1 MB (38119207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b75db0b788ad02c6e5889ddba70f0665ddad45d6497bab5dde6cd3bc8a75498`  
		Last Modified: Wed, 27 May 2026 22:41:26 GMT  
		Size: 90.5 MB (90537364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad46a640bb807424b943a0280255231449df31a13f27361502e40cba9bc6198`  
		Last Modified: Wed, 27 May 2026 22:41:24 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef0184b7d4604c09c8998694d9ab4a56568884728bbf28a87f97169fb2de482`  
		Last Modified: Wed, 27 May 2026 22:41:24 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d53fc6b8c098a559774fd797f3e845385deaf16c41bea15baea76014d7a2300`  
		Last Modified: Wed, 27 May 2026 23:10:26 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ff85daefe2c651f25a39744955725c118e5ee839074cc2c5287a032e01603a`  
		Last Modified: Wed, 27 May 2026 23:10:27 GMT  
		Size: 42.0 MB (41958466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac14eee5dd343eb20eedc09b81e4c9a54d349dad5747c07193641b107e9ae173`  
		Last Modified: Wed, 27 May 2026 23:10:29 GMT  
		Size: 140.2 MB (140236991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaca787f3c38fff6895e72c5c5704cfc6bdc651a02e0103e90e5dbfe895143d`  
		Last Modified: Wed, 27 May 2026 23:10:26 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:5d5e8b6ccce65aaecf83f6de8d39110915c19d9a44fbdcf117bc5868ccd43b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7031871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5866ff9b838428f98f6d202cef8f83ea87c1288f998b161b61f3d7f0b3b0fa`

```dockerfile
```

-	Layers:
	-	`sha256:8b0dbd0cfef72f60a4364fe3a8b8c23029e70b586cbfd086a01fea8fa8bcb9f9`  
		Last Modified: Wed, 27 May 2026 23:10:26 GMT  
		Size: 7.0 MB (7007452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16d148b0e5a0775a46e1dbf3e4bfb56c022ad532b0b8027ac65d3ee5640d8b63`  
		Last Modified: Wed, 27 May 2026 23:10:26 GMT  
		Size: 24.4 KB (24419 bytes)  
		MIME: application/vnd.in-toto+json
