## `gradle:9-jdk17-ubi9`

```console
$ docker pull gradle@sha256:0b9fe9a00fcc8d6f2f6f669b54259f6bab2e6da5788ae43a09d9f945d79313b6
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

### `gradle:9-jdk17-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:e3a80ace3043ceec909e0f8de02a7eecd08d32b1222be738f30ea633beb16ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 MB (390546348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71af8cd6d22e53716801c9bae94f99a0964030675e34d6bd6c2e49804ba7c54`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:51:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:51:30 GMT
ENV container oci
# Wed, 11 Mar 2026 04:51:31 GMT
COPY dir:c1ba4c335e7831ddebf5732b67e3739a636a3d3dbf6b4d4089ed8f31a1bfbfd1 in /      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:51:31 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:31 GMT
COPY file:53f3c4e4ec21f021024505adc7a7710e18079e2a86f12f898f971cadc64b7478 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:51:32 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:51:18Z" "org.opencontainers.image.created"="2026-03-11T04:51:18Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:51:18Z
# Wed, 11 Mar 2026 18:34:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Mar 2026 18:34:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:34:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 18:34:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:34:41 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 11 Mar 2026 18:34:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 11 Mar 2026 18:34:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 11 Mar 2026 18:34:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:34:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Mar 2026 18:34:49 GMT
CMD ["jshell"]
# Wed, 11 Mar 2026 19:12:59 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:12:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:12:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:12:59 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:12:59 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:13:03 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 11 Mar 2026 19:13:03 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 11 Mar 2026 19:13:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 11 Mar 2026 19:13:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:13:06 GMT
USER gradle
# Wed, 11 Mar 2026 19:13:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 11 Mar 2026 19:13:06 GMT
USER root
```

-	Layers:
	-	`sha256:1174ed37633caad5219e59c67f05fe4e54bd728c7a8cfd4ea1df16de15de2f76`  
		Last Modified: Wed, 11 Mar 2026 06:07:51 GMT  
		Size: 40.0 MB (39990896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eb16625353f69ce3344cb87bfa2b43084aeab91a8dfa2c3d378c1b8c58e181`  
		Last Modified: Wed, 11 Mar 2026 18:35:08 GMT  
		Size: 30.4 MB (30394396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f94d0fcceba41b2d65134570dff22b296fc27abf2c4cb06664ea52c7351efa`  
		Last Modified: Wed, 11 Mar 2026 18:35:11 GMT  
		Size: 145.6 MB (145637127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806c9691495b65fc7b293b9016b8d81e3b065520f416db1c12a4f3997dc06fcb`  
		Last Modified: Wed, 11 Mar 2026 18:35:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4aa78604a751da69913524ca048b619d0620059d1ca1508cde5d6c41b8564a`  
		Last Modified: Wed, 11 Mar 2026 18:35:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a06c69a19b31b4d2488dafc79b6b6734860c52ebc28c4b4e53736a7aa7298f4`  
		Last Modified: Wed, 11 Mar 2026 19:13:23 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029d8ca1515e1808dede47e138ddc11d77c66f987123b0037a84086d0d64d860`  
		Last Modified: Wed, 11 Mar 2026 19:13:26 GMT  
		Size: 36.7 MB (36721004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4abcbbb75fed304c7217effd1b87028ad07294dcf3bbed4ef9a48dc26b3797`  
		Last Modified: Wed, 11 Mar 2026 19:13:31 GMT  
		Size: 137.8 MB (137773155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c051cec279478f16c5559c9a2173e4f468a212f80c0df3a95b663a17576815`  
		Last Modified: Wed, 11 Mar 2026 19:13:24 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:524a0bf30ac9867f69a2d3a757a4d1b371cec0f5f0a335c2d13c9539e88dd3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5412238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af8b6f6cb876610fe75bd3f2ed12ba800e3c258f8b0187c35ae825ebb709f49f`

```dockerfile
```

-	Layers:
	-	`sha256:c8518eeabe73294ee8793e945279b3a3ef91c7d9d5d1cb0a08226ecbf052dafe`  
		Last Modified: Wed, 11 Mar 2026 19:13:24 GMT  
		Size: 5.4 MB (5389042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357cafb69ea6eb3c4a15e1325a50cb12da241b604e33449001fdbe1de39945cf`  
		Last Modified: Wed, 11 Mar 2026 19:13:23 GMT  
		Size: 23.2 KB (23196 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9826367012713fad2aec22f82146ad912d8ba7211e5948c218d08571c1011ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387337306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83480078397b4bcfc45bc6e2e3f2407305577d3b05eaca98371ff39e094e216f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:19 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:19 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:20 GMT
COPY dir:7796b64b73526e8dad6fca20071cfe57334a57323fbbb1f9256c4ffffa8b27db in /      
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:20 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:20 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
COPY file:186c4202737062dc84f1db98b633710a412a23c003ba73ff6ae51d727aea1cd8 in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:53:21 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:07Z" "org.opencontainers.image.created"="2026-03-11T04:53:07Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:07Z
# Wed, 11 Mar 2026 18:34:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Mar 2026 18:34:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:34:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 18:34:30 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:34:30 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 11 Mar 2026 18:34:37 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 11 Mar 2026 18:34:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 11 Mar 2026 18:34:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:34:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Mar 2026 18:34:38 GMT
CMD ["jshell"]
# Wed, 11 Mar 2026 19:13:04 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:13:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:13:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:13:04 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:13:04 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:13:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 11 Mar 2026 19:13:08 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 11 Mar 2026 19:13:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 11 Mar 2026 19:13:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:13:11 GMT
USER gradle
# Wed, 11 Mar 2026 19:13:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 11 Mar 2026 19:13:11 GMT
USER root
```

-	Layers:
	-	`sha256:a929c158045efa38dcdfac5809dfda6e7c13c225e0aae109412941b4ed8f3880`  
		Last Modified: Wed, 11 Mar 2026 06:07:49 GMT  
		Size: 38.2 MB (38205467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007b147084be85d4299144a7904cf87b672bdce01f5355daf402b74807d53fe0`  
		Last Modified: Wed, 11 Mar 2026 18:34:56 GMT  
		Size: 30.8 MB (30824795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de51f0ea91b6486aefe87783e6ab589660e7f13098c1ba51f864e9a6417fa283`  
		Last Modified: Wed, 11 Mar 2026 18:34:58 GMT  
		Size: 144.4 MB (144446559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6364a52671e08ea4f59e960a088290a082d93c4bd6badb47673bf71d201f418c`  
		Last Modified: Wed, 11 Mar 2026 18:34:54 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1180686e8e7571cca73b89a114c11fd09473d7c83ee5edf417250e14bc931004`  
		Last Modified: Wed, 11 Mar 2026 18:34:54 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc3d191548f0bb286d1c4194ab83ffff371d88a59c07252dcceae693b6a924a`  
		Last Modified: Wed, 11 Mar 2026 19:13:28 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d3c41028e7b966ef2efa0e8da6983c966d52ed95a7b799c059dd0a26550640`  
		Last Modified: Wed, 11 Mar 2026 19:13:30 GMT  
		Size: 36.1 MB (36053833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee1d144e1973708d40c01e59014819f2b01ccc510388facb05c66d60ec860a7`  
		Last Modified: Wed, 11 Mar 2026 19:13:32 GMT  
		Size: 137.8 MB (137773160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2787ff686e5fcdfcc84c5c42c6eb780883da19b560d8ee496b0bc8fa94f6a7d`  
		Last Modified: Wed, 11 Mar 2026 19:13:28 GMT  
		Size: 29.3 KB (29332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:756d88c613a1bdeba447ba48da225612f43bcdda1b78be6d3497ad146e30c344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5411769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d1563e895b3333868baa536633f02e6fc4123414a71330e53e359435412826`

```dockerfile
```

-	Layers:
	-	`sha256:a4d392e3740b12967ccce51b7a7fd58cf6c49390fceae84cd801c5cefd33df51`  
		Last Modified: Wed, 11 Mar 2026 19:13:28 GMT  
		Size: 5.4 MB (5388424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:596afd1f8da8ae07df5534427582c292aac379ce21c1ca83866d165d83e22e90`  
		Last Modified: Wed, 11 Mar 2026 19:13:28 GMT  
		Size: 23.3 KB (23345 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:ee0ac7c617f9abbf976c7903f0146b1a93b5b64ddeb6a3b96710dc6905584f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398524915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7f59c47cc64c2f7db7b706ed055da03a47139ce9be5390ebaf2b33cf050c53`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 04:53:58 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 04:53:58 GMT
ENV container oci
# Wed, 11 Mar 2026 04:53:59 GMT
COPY dir:c16ffb4ff368c4c4701379220271e573fd98f7ef429754d838e4da274182d3d4 in /      
# Wed, 11 Mar 2026 04:53:59 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 04:53:59 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 04:53:59 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 04:53:59 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 04:53:59 GMT
COPY file:96735fc1d76fbe7cf3c45c3807304493b83949ae77c293c442c668195fa626bc in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:54:00 GMT
COPY file:96735fc1d76fbe7cf3c45c3807304493b83949ae77c293c442c668195fa626bc in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 04:54:00 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T04:53:48Z" "org.opencontainers.image.created"="2026-03-11T04:53:48Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T04:53:48Z
# Wed, 11 Mar 2026 18:32:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Mar 2026 18:32:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:32:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 18:32:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:32:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 11 Mar 2026 18:34:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 11 Mar 2026 18:34:32 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 11 Mar 2026 18:34:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:34:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Mar 2026 18:34:32 GMT
CMD ["jshell"]
# Wed, 11 Mar 2026 19:11:12 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:11:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:11:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:11:12 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:11:13 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:11:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 11 Mar 2026 19:11:26 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 11 Mar 2026 19:11:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 11 Mar 2026 19:11:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:11:33 GMT
USER gradle
# Wed, 11 Mar 2026 19:11:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 11 Mar 2026 19:11:34 GMT
USER root
```

-	Layers:
	-	`sha256:6121bae13aca039c044ec77f6c0d5c8628a9f1a6cb6026e98347fb488c0c92d1`  
		Last Modified: Wed, 11 Mar 2026 06:10:11 GMT  
		Size: 44.5 MB (44455609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f2be856b2fb1b1a7acb76036ea4b0ce4d3c01cf5e16be0f3a42cebc98397f1`  
		Last Modified: Wed, 11 Mar 2026 18:33:12 GMT  
		Size: 32.9 MB (32872967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c791126219d7bd5e835180ae53e296812cbc6f2ab2ac0cf0b1700761312b26f8`  
		Last Modified: Wed, 11 Mar 2026 18:35:11 GMT  
		Size: 145.5 MB (145459974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dbfc0007e03d3a4442ab27b274d06147d8a7573103665ba0a3f88e372a7525`  
		Last Modified: Wed, 11 Mar 2026 18:35:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7dfc11766888cb1d4b0cfbab7ea30c992a3d75d66f396ecf5273e5d9440c2`  
		Last Modified: Wed, 11 Mar 2026 18:35:07 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bb61f95a73af6476bd9190e321990ffa0d894d50a7719fff6fcd23ca3c1b41`  
		Last Modified: Wed, 11 Mar 2026 19:12:19 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087a3f6527c166a1ccb81d7f4d33e1ce0161331c242e8fca3990eb02a997bd0d`  
		Last Modified: Wed, 11 Mar 2026 19:12:21 GMT  
		Size: 38.0 MB (37958662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6708f0d451b8bade507316449207537e64998c67c53ec753cdb2ffbfe69e02f3`  
		Last Modified: Wed, 11 Mar 2026 19:12:23 GMT  
		Size: 137.8 MB (137773162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50123b3846750f23e377b2b9219db386aa72077cc32bb80b6626c8b9718c25ca`  
		Last Modified: Wed, 11 Mar 2026 19:12:19 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:0ab52df55a91e3dc01b3a01c1e15e8ec6c971b8db0a84264019b289b05ced252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5409633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124ab442b69a00da9f7c8171904a1c8f222f8acac941e732da5b67f9834ed98a`

```dockerfile
```

-	Layers:
	-	`sha256:04114293aabac2d7622bd06245db20fa5766282b5a16272d5ebe3f29fb267a4a`  
		Last Modified: Wed, 11 Mar 2026 19:12:19 GMT  
		Size: 5.4 MB (5386353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4dd39faa99661c568684c831faf3b7ccd51e6ab4aaa6f7328e02bee6363d93d`  
		Last Modified: Wed, 11 Mar 2026 19:12:19 GMT  
		Size: 23.3 KB (23280 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:365a804f6a7a1b761b587fc294d7df9ecd0382053b0959672ac70df071b71b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.3 MB (378281989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7bbb15cea3a7452bf27f4c429fc49733558935611096b42e3bdcebd67bab79`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 11 Mar 2026 05:09:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 11 Mar 2026 05:09:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 11 Mar 2026 05:09:06 GMT
ENV container oci
# Wed, 11 Mar 2026 05:09:06 GMT
COPY dir:a75f302c58b91e03eb462e96994a66e692bdd08299caf4a5879a83dc26c33c54 in /      
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 11 Mar 2026 05:09:06 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:94e309aff1f0192ed947120fc4293382d72a8b466c1a32dde7e4ec5ddd2c8d6c in /usr/share/buildinfo/labels.json      
# Wed, 11 Mar 2026 05:09:06 GMT
COPY file:94e309aff1f0192ed947120fc4293382d72a8b466c1a32dde7e4ec5ddd2c8d6c in /root/buildinfo/labels.json      
# Wed, 11 Mar 2026 05:09:07 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="ddf3e9d218968613397a7b4df7547f25ad755449" "org.opencontainers.image.revision"="ddf3e9d218968613397a7b4df7547f25ad755449" "build-date"="2026-03-11T05:08:54Z" "org.opencontainers.image.created"="2026-03-11T05:08:54Z" "release"="1773204619"org.opencontainers.image.revision=ddf3e9d218968613397a7b4df7547f25ad755449,org.opencontainers.image.created=2026-03-11T05:08:54Z
# Wed, 11 Mar 2026 18:27:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Mar 2026 18:27:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Mar 2026 18:27:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Mar 2026 18:27:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 11 Mar 2026 18:27:45 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 11 Mar 2026 18:27:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 11 Mar 2026 18:27:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 11 Mar 2026 18:27:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:27:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Mar 2026 18:27:53 GMT
CMD ["jshell"]
# Wed, 11 Mar 2026 19:11:06 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:11:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:11:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:11:06 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:11:06 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:11:12 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 11 Mar 2026 19:11:12 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 11 Mar 2026 19:11:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 11 Mar 2026 19:11:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:11:16 GMT
USER gradle
# Wed, 11 Mar 2026 19:11:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 11 Mar 2026 19:11:16 GMT
USER root
```

-	Layers:
	-	`sha256:8b6042692ebd14654705cc63a2e114754df79af319b19ae7d1c0200f6929153c`  
		Last Modified: Wed, 11 Mar 2026 06:10:02 GMT  
		Size: 38.1 MB (38114066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ef867c0faa45e8e1b1c5c9279c4cb5cd1df03b22f576609452f5921f4182cf`  
		Last Modified: Wed, 11 Mar 2026 18:28:09 GMT  
		Size: 30.4 MB (30416196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7398c6f2a83d988a447483bdb0499bee506311751d30f6aede234e5b5675c26a`  
		Last Modified: Wed, 11 Mar 2026 18:28:21 GMT  
		Size: 135.6 MB (135629094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a87fed9d48e96ce0daafe80c5d16cacf95391ff90c91af483bc168b0786d8`  
		Last Modified: Wed, 11 Mar 2026 18:28:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7b4403b6438a7dacca77707a8dc2f0233bedc8380ff40160461e2cdc00444b`  
		Last Modified: Wed, 11 Mar 2026 18:28:17 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c5bcc98f91a4574d49318114ba2ba179cb698fe006a7d0c821d4cb33ede84a`  
		Last Modified: Wed, 11 Mar 2026 19:11:40 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797f648898c5e02998ebb4082d6d76fbbfb8610837694ed1fe3ddde44dfa62c1`  
		Last Modified: Wed, 11 Mar 2026 19:11:42 GMT  
		Size: 36.3 MB (36344942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a382bd09691ea1165898888800eaed1f72d16144671e83eb4c92e796725d94`  
		Last Modified: Wed, 11 Mar 2026 19:11:44 GMT  
		Size: 137.8 MB (137773160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ee162d39cc05175df4ad1c97ec6b9bfae97115c327a7dd9286fa00c2df4257`  
		Last Modified: Wed, 11 Mar 2026 19:11:41 GMT  
		Size: 373.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:94a176ec5f6a2673edbf5551a043ae29f4cc85ab43519c8f4879adfffc58efd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19eb2c3671a4a301da04d66770375d304e950e37a56a2c15ac6f61e48d71135b`

```dockerfile
```

-	Layers:
	-	`sha256:65fc0ea6557ee419d4ad618da3e78e8a827a45b3d8245ab55a70f043e0ccb3a7`  
		Last Modified: Wed, 11 Mar 2026 19:11:41 GMT  
		Size: 5.4 MB (5375647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49fd97f3b7d13ebe4b8aa5c994e8346b80ac2c141e068670a129dc3030569a7f`  
		Last Modified: Wed, 11 Mar 2026 19:11:40 GMT  
		Size: 23.2 KB (23229 bytes)  
		MIME: application/vnd.in-toto+json
