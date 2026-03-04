## `gradle:jdk21-ubi`

```console
$ docker pull gradle@sha256:b24ba13d70fd85982dfa51bbd55dbc3aaa16aa4007f8f313253c17d15e4af923
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

### `gradle:jdk21-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:62bc72129f27736bf35c614bb715d0ddd388f1a1c0c0793a69802f5cba97e64f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.4 MB (406435845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a8e7337a5b17fbb895c03f54c117cca7e55d3f6cfc9c4385c018c38b3551b6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 08:55:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 08:55:55 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 08:55:55 GMT
ENV container oci
# Mon, 02 Mar 2026 08:55:55 GMT
COPY dir:bc9a8a44e634605c4ff89328666c26f0c256afabea6c375c1017a88a80500ea2 in /      
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 08:55:55 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 08:55:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 08:55:56 GMT
COPY file:c0327936eac36593f0ab8d7da594e1a816cbe84da917c4d0a34bfcc7a914e024 in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:55:56 GMT
COPY file:c0327936eac36593f0ab8d7da594e1a816cbe84da917c4d0a34bfcc7a914e024 in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:55:56 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T08:55:38Z" "org.opencontainers.image.created"="2026-03-02T08:55:38Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T08:55:38Z
# Mon, 02 Mar 2026 22:05:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:05:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:05:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:05:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:05:09 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 02 Mar 2026 22:06:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:06:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:06:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:06:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:06:03 GMT
CMD ["jshell"]
# Wed, 04 Mar 2026 17:54:16 GMT
CMD ["gradle"]
# Wed, 04 Mar 2026 17:54:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Mar 2026 17:54:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Mar 2026 17:54:16 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Mar 2026 17:54:16 GMT
WORKDIR /home/gradle
# Wed, 04 Mar 2026 17:54:20 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 04 Mar 2026 17:54:20 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 04 Mar 2026 17:54:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 04 Mar 2026 17:54:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Mar 2026 17:54:23 GMT
USER gradle
# Wed, 04 Mar 2026 17:54:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 04 Mar 2026 17:54:23 GMT
USER root
```

-	Layers:
	-	`sha256:4377b1aab54b81e1e3b39331172fb1424f433cdfe28e8bf6f9cd313a971d0d61`  
		Last Modified: Mon, 02 Mar 2026 10:45:10 GMT  
		Size: 34.6 MB (34610905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f276e3eb8f3d45a8ee4d3cba66d483e300e92657d38599052823f1d516f222e4`  
		Last Modified: Mon, 02 Mar 2026 22:05:28 GMT  
		Size: 37.4 MB (37429238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827ae1c10d500c64ac3da3752a9c470834c288c91c501d0926ce0cb02ac7ec81`  
		Last Modified: Mon, 02 Mar 2026 22:06:23 GMT  
		Size: 157.9 MB (157861009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296754410aaa11c057c63cad164af72631744ba68e29655a87520b1afdc7dc0a`  
		Last Modified: Mon, 02 Mar 2026 22:06:20 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2e04ad7dc6c76f98b7341f04a39698dc2721d4349090216cb5b9dd10a3bd0f`  
		Last Modified: Mon, 02 Mar 2026 22:06:20 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d47b60af242b9601aa2dedf0d7a780e2a6c03d5fe88d8b9002ee24e9afc481`  
		Last Modified: Wed, 04 Mar 2026 17:54:40 GMT  
		Size: 1.6 KB (1589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731cb749f7c5596992e1a21c4078f2e878ccbbf62ad851423bb88fac3edd705b`  
		Last Modified: Wed, 04 Mar 2026 17:54:42 GMT  
		Size: 38.7 MB (38731879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9a1186aec5d3cf964688b7b03ea53f0784a3f1007ecf57cd2f7aecd79ea5c9`  
		Last Modified: Wed, 04 Mar 2026 17:54:44 GMT  
		Size: 137.8 MB (137773162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe495e74c407692592443b663175445b9a9e22f982f82c4fcbf946ba51d0d2`  
		Last Modified: Wed, 04 Mar 2026 17:54:41 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:3a4e5ea79f9110fe01b5475c0944c059c9447ee6483c3dfcc1481a9792c75f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7053213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df265aad7b2e5965306b138e4269f9fbde354fdf4bb5eba01f4b2b0c1578d113`

```dockerfile
```

-	Layers:
	-	`sha256:0ee8e32ec799e7393c2ad55cefea842d4b8baef6b90e369089246b6cbdd2d421`  
		Last Modified: Wed, 04 Mar 2026 17:54:41 GMT  
		Size: 7.0 MB (7028762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de89251aee59cbfa96a01cd19b0d70d1f84e2a67f48855396c727235e41d50eb`  
		Last Modified: Wed, 04 Mar 2026 17:54:40 GMT  
		Size: 24.5 KB (24451 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:288f031dd8b36955fd7748a7e1b8343b1fdc021febe2caeab4f44a368c47f2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.2 MB (402229494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbee59bd9e40d0cc2a1405669a825937eb7f32e3124b85c81cf2fc714c35dca6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 08:58:05 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 08:58:05 GMT
ENV container oci
# Mon, 02 Mar 2026 08:58:06 GMT
COPY dir:c8a0e6b85769dc5b1153f2d95c0dab0c21c76be6878d56a453a175f235aec4f0 in /      
# Mon, 02 Mar 2026 08:58:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 08:58:06 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:09f44631adf2e487fe312f2a1e81a1022d21dd1ab82974e6dcdb1c9761ad2ce6 in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:58:07 GMT
COPY file:09f44631adf2e487fe312f2a1e81a1022d21dd1ab82974e6dcdb1c9761ad2ce6 in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 08:58:07 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T08:57:50Z" "org.opencontainers.image.created"="2026-03-02T08:57:50Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T08:57:50Z
# Mon, 02 Mar 2026 22:08:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:08:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:08:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:08:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:08:14 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 02 Mar 2026 22:09:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:09:08 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:09:08 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:09:08 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:09:08 GMT
CMD ["jshell"]
# Wed, 04 Mar 2026 17:53:44 GMT
CMD ["gradle"]
# Wed, 04 Mar 2026 17:53:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Mar 2026 17:53:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Mar 2026 17:53:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Mar 2026 17:53:44 GMT
WORKDIR /home/gradle
# Wed, 04 Mar 2026 17:53:49 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 04 Mar 2026 17:53:49 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 04 Mar 2026 17:53:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 04 Mar 2026 17:53:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Mar 2026 17:53:52 GMT
USER gradle
# Wed, 04 Mar 2026 17:53:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 04 Mar 2026 17:53:52 GMT
USER root
```

-	Layers:
	-	`sha256:ab71f30be3b758ee5a6fbf5d72df781f51e8cf5753ddf02671b2d7e13e4932fb`  
		Last Modified: Mon, 02 Mar 2026 11:28:23 GMT  
		Size: 32.7 MB (32683006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3889f3884aa943c26e1c1b3de15da7a5aebe5f569d872cc163230b47be37b7`  
		Last Modified: Mon, 02 Mar 2026 22:08:32 GMT  
		Size: 37.4 MB (37374475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8424ff744137f0d69dadc7dc6e139833c657583ecdbf1354a5437fab16096336`  
		Last Modified: Mon, 02 Mar 2026 22:09:28 GMT  
		Size: 156.1 MB (156136202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07deadb2ca749914d5586c21915b7a392533d88f4682722819df7ef3397b28b7`  
		Last Modified: Mon, 02 Mar 2026 22:09:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f137add0773cd301526b67b6d55f23bfe29b02feab165412ca6e9472f5715e61`  
		Last Modified: Mon, 02 Mar 2026 22:09:26 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ef113c9904019eae2ac2ac9d6988503df386f48bdba02e49516f54849e7d09`  
		Last Modified: Wed, 04 Mar 2026 17:54:11 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca05cf941a5261fea860f8f7ae1873b6303d64e6685025e894228a6c2f87f10`  
		Last Modified: Wed, 04 Mar 2026 17:54:13 GMT  
		Size: 38.2 MB (38229272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40943c6d517ba73f9c6d3c667859b3cc1f74d2821e8f23ccf862cba0097de207`  
		Last Modified: Wed, 04 Mar 2026 17:54:16 GMT  
		Size: 137.8 MB (137773163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd62983f4337f81e71f11e49518f8ed94fee4288b1e8b8a1157296aa568acaf`  
		Last Modified: Wed, 04 Mar 2026 17:54:11 GMT  
		Size: 29.3 KB (29339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:355edcb0693413aa0371c9b0dc8e285e25c35caadd2620d1329a93949b7150f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7051666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:682066d5cee72b2b90b7bc3f9c8e84cafda3f3747dddced1b06b586b0f364881`

```dockerfile
```

-	Layers:
	-	`sha256:a1717629a40307a056c163061bcc80527360774691e0c9c30c80e4ed1351ea53`  
		Last Modified: Wed, 04 Mar 2026 17:54:12 GMT  
		Size: 7.0 MB (7027018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c64d0afbe60781e50fb3ef0ac21cd2a8d197b16d5bc81985a869db12cc21aa2`  
		Last Modified: Wed, 04 Mar 2026 17:54:12 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:f9dbf7f1cbff464a35131af649b95ff3d05726ff709a7806493817e05bd58e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.1 MB (414136941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03683bd0b0eb1965bab6f73df35267f3aa301ff1c4224563e3cc87e77ae62963`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 09:04:59 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 09:04:59 GMT
ENV container oci
# Mon, 02 Mar 2026 09:05:00 GMT
COPY dir:e20d8c9b5112eae2ec3cf27567703617b532b3d50e37e22798356175a81af012 in /      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 09:05:00 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:f249adc52ffecf442b4262c353b6483cbd86a0119b4a0d56c2ae3482dda5e6dd in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:05:00 GMT
COPY file:f249adc52ffecf442b4262c353b6483cbd86a0119b4a0d56c2ae3482dda5e6dd in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:05:01 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T09:04:48Z" "org.opencontainers.image.created"="2026-03-02T09:04:48Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T09:04:48Z
# Mon, 02 Mar 2026 22:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:11:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:11:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:11:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:11:17 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 02 Mar 2026 22:14:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:14:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:14:15 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:14:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:14:15 GMT
CMD ["jshell"]
# Wed, 04 Mar 2026 18:26:41 GMT
CMD ["gradle"]
# Wed, 04 Mar 2026 18:26:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Mar 2026 18:26:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Mar 2026 18:26:41 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Mar 2026 18:26:42 GMT
WORKDIR /home/gradle
# Wed, 04 Mar 2026 18:27:10 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 04 Mar 2026 18:27:10 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 04 Mar 2026 18:27:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 04 Mar 2026 18:27:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Mar 2026 18:27:16 GMT
USER gradle
# Wed, 04 Mar 2026 18:27:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 04 Mar 2026 18:27:19 GMT
USER root
```

-	Layers:
	-	`sha256:52175d44fca07e14e1039fd9cb5b5c7a4f5a641951f3018cac642ab2b0d7aa2d`  
		Last Modified: Mon, 02 Mar 2026 12:12:22 GMT  
		Size: 38.7 MB (38730989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40df108a302998b0b0c1beb639de829388ba26f170d0578e18c4fcfeb7e8204b`  
		Last Modified: Mon, 02 Mar 2026 22:11:53 GMT  
		Size: 39.2 MB (39183318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6db1b50cb23cc81782f1e68ab4925664465988bacdf8e99354a09bb48837ef7`  
		Last Modified: Mon, 02 Mar 2026 22:15:03 GMT  
		Size: 158.0 MB (157981336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36798030e22ecd09ea3913a7627d209fd31e011fb52f14b3be6b066935518e08`  
		Last Modified: Mon, 02 Mar 2026 22:14:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04d48866363f99add341fb489417035c913c593acc5778e3309b47b7c14dd1b`  
		Last Modified: Mon, 02 Mar 2026 22:14:54 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4c9b2e625401cc4ee4f87717b8f21e564c31ecfea40397307d0765647d5a9a`  
		Last Modified: Wed, 04 Mar 2026 18:28:05 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f5fe835a58c7898ac99ab498e53e349b27dfe66a74bdbf1ab79ba26969167`  
		Last Modified: Wed, 04 Mar 2026 18:28:07 GMT  
		Size: 40.5 MB (40463761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd759a29d2802ff485275014185df01a0d0ba455cd524550e085721ebaff547`  
		Last Modified: Wed, 04 Mar 2026 18:28:10 GMT  
		Size: 137.8 MB (137773119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c1dbc1e2d2d4a56c6af736cd0b29b4f51a32cc01d82d15c963b37706e11470`  
		Last Modified: Wed, 04 Mar 2026 18:28:05 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:8024ade3ca9b1b687ee6af471bb96426b080a6c1fe5904f706f00e3a4412fb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7044703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6303155cf3899d4a0a36edd00809111238ae1de9861acffa96e86598611ac542`

```dockerfile
```

-	Layers:
	-	`sha256:04e85c581fe67333c22bbc42d026854807b2f44ee86dea77483a34e927f1382b`  
		Last Modified: Wed, 04 Mar 2026 18:28:06 GMT  
		Size: 7.0 MB (7020180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798037b88d4d4ec2b4da0392141e62b82833c14c56f2e444f238a998abdb85e0`  
		Last Modified: Wed, 04 Mar 2026 18:28:05 GMT  
		Size: 24.5 KB (24523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:9b0096e6972ce639ecf6b762b67f124b9aba46439d940658c449869365ee8a64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.9 MB (397930993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff38caa78d6372e37af8e8a554b2c4e725b7af31b06fd4b6c66625c6dbb1c9ed`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Mar 2026 09:51:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Mon, 02 Mar 2026 09:51:06 GMT
ENV container oci
# Mon, 02 Mar 2026 09:51:07 GMT
COPY dir:5dd35d5c1dec7b82721f4ea46a7d4cf99ee4456a5024db00ef7a4185cd459224 in /      
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Mon, 02 Mar 2026 09:51:07 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:3bfe8a93182a824c0d137026e37cb062ae718ca91203068e33c3ca4c98e5db8a in /usr/share/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:51:07 GMT
COPY file:3bfe8a93182a824c0d137026e37cb062ae718ca91203068e33c3ca4c98e5db8a in /root/buildinfo/labels.json      
# Mon, 02 Mar 2026 09:51:07 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="22680d9fff6e4cead236be943e791fde5247c69a" "org.opencontainers.image.revision"="22680d9fff6e4cead236be943e791fde5247c69a" "build-date"="2026-03-02T09:50:54Z" "org.opencontainers.image.created"="2026-03-02T09:50:54Z" "release"="1772441549"org.opencontainers.image.revision=22680d9fff6e4cead236be943e791fde5247c69a,org.opencontainers.image.created=2026-03-02T09:50:54Z
# Mon, 02 Mar 2026 22:06:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 22:06:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 22:06:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Mar 2026 22:06:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Mon, 02 Mar 2026 22:06:18 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Mon, 02 Mar 2026 22:07:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Mar 2026 22:07:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Mar 2026 22:07:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Mar 2026 22:07:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Mar 2026 22:07:14 GMT
CMD ["jshell"]
# Wed, 04 Mar 2026 17:58:25 GMT
CMD ["gradle"]
# Wed, 04 Mar 2026 17:58:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 04 Mar 2026 17:58:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 04 Mar 2026 17:58:25 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 04 Mar 2026 17:58:25 GMT
WORKDIR /home/gradle
# Wed, 04 Mar 2026 17:58:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 04 Mar 2026 17:58:31 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 04 Mar 2026 17:58:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 04 Mar 2026 17:58:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 04 Mar 2026 17:58:34 GMT
USER gradle
# Wed, 04 Mar 2026 17:58:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 04 Mar 2026 17:58:35 GMT
USER root
```

-	Layers:
	-	`sha256:994f616032f72d0ca9e8101a9d46009ec833cad6f73762dc4e8b95e1492b92d5`  
		Last Modified: Mon, 02 Mar 2026 12:12:14 GMT  
		Size: 34.4 MB (34388694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c78511c21b0da95cf534d58ef20e248f21114652f106ce5c6bb3ffc8ab5984`  
		Last Modified: Mon, 02 Mar 2026 22:06:47 GMT  
		Size: 37.8 MB (37811658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecb2d4393f4df92f14abc524b6797c475180fed63a66411f1adab6c12f2bcaa`  
		Last Modified: Mon, 02 Mar 2026 22:07:46 GMT  
		Size: 147.1 MB (147104839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b54a98b13be16e8bed5f89516dc85c63527b6529936688193bd1358e4ceef6`  
		Last Modified: Mon, 02 Mar 2026 22:07:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18092f97af5473d1416973de0781898566995dce2350bcf7f415f3d47ffe242b`  
		Last Modified: Mon, 02 Mar 2026 22:07:43 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acad68395a6d33cad77a7c29262608c4c04d6fe6bb6b97ce6fc8d0ef06addfc4`  
		Last Modified: Wed, 04 Mar 2026 17:59:03 GMT  
		Size: 1.6 KB (1588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3e350b9b99615779bc59b8db232a01cb3777c5cde7ff57820c27e711f8df76`  
		Last Modified: Wed, 04 Mar 2026 17:59:04 GMT  
		Size: 40.8 MB (40848228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de231758dbbf7513269a9296469d4f01f48046108e180fc31580249b520b65f`  
		Last Modified: Wed, 04 Mar 2026 17:59:06 GMT  
		Size: 137.8 MB (137773159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88729640788cffe42d72b504a58eadcc92d614bdadcbd93fe46ab0c637dcb08`  
		Last Modified: Wed, 04 Mar 2026 17:59:03 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:3010d5880788c601abd378171a24c7f898636e76895b9bef3e02da33644a3bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7033858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24965ff2c4e9a3c1ddecd192cdad9add1549811ef4ad23611bbca0d1b422bf41`

```dockerfile
```

-	Layers:
	-	`sha256:5029b2442629ea2750c1731330b9d4b8f1a781059db8c85a1bab037851d82a4c`  
		Last Modified: Wed, 04 Mar 2026 17:59:03 GMT  
		Size: 7.0 MB (7009409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2e5d07afce6935b55006c7c2a0ac3c3d72c1cdcd3b3bd3c8fd1ab360e58ac6a`  
		Last Modified: Wed, 04 Mar 2026 17:59:03 GMT  
		Size: 24.4 KB (24449 bytes)  
		MIME: application/vnd.in-toto+json
