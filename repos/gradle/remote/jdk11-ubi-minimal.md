## `gradle:jdk11-ubi-minimal`

```console
$ docker pull gradle@sha256:f3c6cdf52f5cbe782f2995dbde2b2c80afd9d861949e6e9eb90ac70c0b6005f4
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

### `gradle:jdk11-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:d8d5ac43fe82bfc48779e6fb64fe3d9be8eb88f02ac2df31cd829f9c70026a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.5 MB (383544962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f378881b56f0446be2d1a3b2c645bfbae475f7876d93cdd780157b8f9df8cee`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:dca6230157d1db8824aac8b8e02a58f86449d038270aad6f0997ce65db8f8656 in /    
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json    
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-06-30T12:32:07" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64le)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        x86_64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:1ec5864c36114bbcd01f21fd199950f3730f43e1c94cc7b37c7bbf8bd446148d`  
		Last Modified: Mon, 30 Jun 2025 13:22:01 GMT  
		Size: 39.7 MB (39650824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e424d5638f6be74bb1fc818388f1d9f78cbbcc70cdbfb47f7ef0cabfacd675b`  
		Last Modified: Wed, 02 Jul 2025 18:45:01 GMT  
		Size: 27.5 MB (27545328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cd4330f6406624c45e8718dca89ee46aea17a43f3afc795f3025ec8b564e54`  
		Last Modified: Wed, 02 Jul 2025 19:07:38 GMT  
		Size: 142.1 MB (142096847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46d1d0ec6b5edb72e558efd37c1bc976e8d3a75619a4ecd4ca49b103bb37402`  
		Last Modified: Wed, 02 Jul 2025 18:44:58 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd4bf1d7f07aa5a608a557d2930ad200316013fa1cbc7813aaa544e0e973b46`  
		Last Modified: Wed, 02 Jul 2025 18:44:58 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ef66d77d823925af3e894bf8d4b82a5a1d5f3bf0ffc264f083281c707f8863`  
		Last Modified: Wed, 02 Jul 2025 19:08:19 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68698a35b7f1e60a0197d4fd3d841d6016392d11129ca4355f0ab8f8e64ce005`  
		Last Modified: Wed, 02 Jul 2025 19:08:22 GMT  
		Size: 36.8 MB (36797389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6b245e6a8820ae9300f5b6ef1e801d6d0b68f5ac6279738a3e271f56d0d5e5`  
		Last Modified: Wed, 02 Jul 2025 19:08:12 GMT  
		Size: 137.4 MB (137395509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae15e9cfb94ab14df5f064b6b7e8d495149b4ab5318995cf7299896a5c640743`  
		Last Modified: Wed, 02 Jul 2025 19:08:19 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:f16815e90b7f5bfff020cea6afb7c2107c25803dd6733eeea7babecddb90c346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c2cc3e1ed5a15bdef2cd53767bd4cd889fa07e6dbdd6694ca44f1db96b0f30`

```dockerfile
```

-	Layers:
	-	`sha256:99a2e16510e73b402836c8adb9744692443def204b2d843fe0019b5979ed84d4`  
		Last Modified: Wed, 02 Jul 2025 20:21:00 GMT  
		Size: 5.4 MB (5398299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2af9a41036c2e9db8192dcb7a38c038a443ac9ca18445481a79273254f56457`  
		Last Modified: Wed, 02 Jul 2025 20:21:01 GMT  
		Size: 24.3 KB (24278 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3d99b79a5780c8315713cd8992716243e1b6d096460b06fe846378e998e76c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.4 MB (378433671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6425cc2c38411654953d9099f8f0e847d0227798b116c8091e553d2bddaae110`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:4a26990fc6a982252bab47a280479ef21eaa9fb0686b5810bf75da5fc5af7d4f in /    
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-06-30T12:36:52" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64le)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        x86_64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:ffb6dfc9a5fd85e709e0a3428084894621f9e001746e51a54875b13ff103e464`  
		Last Modified: Mon, 30 Jun 2025 14:20:11 GMT  
		Size: 37.9 MB (37864356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6a1092a2205635332a54ac734dff85451b8b157ecf360e0dac334f39f8bc66`  
		Last Modified: Wed, 02 Jul 2025 18:55:37 GMT  
		Size: 28.0 MB (27988461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a7895cc866907d3725da8ab3d44fac4280f172f887bc763a8fb9c633a57d6c`  
		Last Modified: Wed, 02 Jul 2025 18:56:26 GMT  
		Size: 138.9 MB (138884826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f2b4e25a8849cec4a404b51b7b13e9a9f4b65d2052477981dca1662ec0791e`  
		Last Modified: Wed, 02 Jul 2025 18:56:47 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7431b50673ca6fc84ec00320b84f13555af600c73e5f7581c0ea17a3d58544d7`  
		Last Modified: Wed, 02 Jul 2025 18:56:47 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff668941c30949276f47095c0f9483079e4f39efee3fbb1c872cbd541b56332`  
		Last Modified: Wed, 02 Jul 2025 19:44:05 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1ba103bf2661518c1f239fab2be97963d091403775873ca524513ff3920e27`  
		Last Modified: Wed, 02 Jul 2025 19:44:13 GMT  
		Size: 36.2 MB (36236832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aab5e9ce298fc8a2cdd21e1ffa3264836faac3e5ef5855907d797a327f611a1`  
		Last Modified: Wed, 02 Jul 2025 19:43:07 GMT  
		Size: 137.4 MB (137395511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8671a7949585e187ce05f91bebd65a96cf33a8c47a01bec2d7a46364c71185ac`  
		Last Modified: Wed, 02 Jul 2025 19:44:05 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:5931e097c11c55180c61f24fe3b1e7ec28fe3a14e36375669a4a32dbdc8d88e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5422824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094f0f7f05e1da5a63371efc3d8ad5836e1a76299eed0fbe8a8005014886a1ea`

```dockerfile
```

-	Layers:
	-	`sha256:a9bc6e2f5641d103b67e50359385ac98e3403bfd7b4b2740d1a58da84b8f1de6`  
		Last Modified: Wed, 02 Jul 2025 20:21:07 GMT  
		Size: 5.4 MB (5398349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b015899eb9d1257b36a5139b346f7d57e52bb373d37d1b62bbce4d1cf591bae3`  
		Last Modified: Wed, 02 Jul 2025 20:21:08 GMT  
		Size: 24.5 KB (24475 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:6d93bc5acace48bfe54face9c3b33ec1ad9083b087f12128dfcb308439e8da38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378895647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dd86729fdc041bb43e539cec268c2c7887c7569641c505a4ef03bdf18bd93d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:6bd7d090c3df5ed04bb4f3de6886ab9cde9ba5683e238b0ef619fa4cb19ee2cd in /    
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-06-30T12:33:57" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64le)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        x86_64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:75a662397909644d17ddc808886bd00daef2f0268930ee1bde3570354249de79`  
		Last Modified: Mon, 30 Jun 2025 18:10:03 GMT  
		Size: 44.0 MB (44033425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbb185fabf19712b2b2f2b19514d76679a1c0211d43689bddde7ee6ede0d37c`  
		Last Modified: Wed, 02 Jul 2025 18:45:24 GMT  
		Size: 30.0 MB (29981051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241744fdf37384a099b3a77b8b0d174ff82b01849bd39b437dc2fb1d4f7fd54b`  
		Last Modified: Wed, 02 Jul 2025 20:18:37 GMT  
		Size: 129.3 MB (129314605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d15ffa2d5c641e659a956bb40098cc07dbe04ccc1a09d7fff8a2907fcc49f71`  
		Last Modified: Wed, 02 Jul 2025 18:47:47 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f597bbb1fe1cfd33a26515bbc2265a133492b391efb19e65ac90fe059074c497`  
		Last Modified: Wed, 02 Jul 2025 18:47:46 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d190beb4fe8d8aba445f6ae49e9cc6fa1c3243becd29b55edb489a9329991e4f`  
		Last Modified: Wed, 02 Jul 2025 19:12:45 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda79f02b45d9b5014acd85ace53aa2fda2f7bae07e70eb4404c436eef967249`  
		Last Modified: Wed, 02 Jul 2025 19:12:47 GMT  
		Size: 38.1 MB (38131887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3945a67f70b46f5908fe9fbef67df247203b2233c3a77794aba2d0126b2fe1`  
		Last Modified: Wed, 02 Jul 2025 19:12:38 GMT  
		Size: 137.4 MB (137395508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774ada8ec176593945de43b677842e1b06bcaab3dd8e04b2b47eeda115e7c84c`  
		Last Modified: Wed, 02 Jul 2025 19:12:45 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:c28dbcd3c8591a63e072501ebe2da819b479ebf379faeea40cb646467944385c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5419373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1257d7fdf6bef785985ec8f77efb523929879ea4b54482abacf03e49d6d4adb0`

```dockerfile
```

-	Layers:
	-	`sha256:836492edd2d23c392fa045801f4665badf26d8c99fbc003c61bda3ffe1b57df2`  
		Last Modified: Wed, 02 Jul 2025 20:21:13 GMT  
		Size: 5.4 MB (5395021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e5a1f52274455bd37b1f009ab97bbbc45c2ab453a1885b8092eb6cdb5640e14`  
		Last Modified: Wed, 02 Jul 2025 20:21:14 GMT  
		Size: 24.4 KB (24352 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-ubi-minimal` - linux; s390x

```console
$ docker pull gradle@sha256:33bd6a7355021494155f423f27d82cb7ca840ff772a0f91d73acf9dbfd1b911f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361211955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6976c3b395ebc8e1bf494af22e3592b13b93b8e34739d4d3bc30bbdec32d57bd`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL url="https://www.redhat.com"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.expose-services=""
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV container oci
# Wed, 23 Apr 2025 14:48:05 GMT
COPY dir:1b67311835389ffe4ad4ead7fcea317b40582d80cd6ef953967b33a7d5cb65e5 in /    
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/.    
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["/bin/bash"]
# Wed, 23 Apr 2025 14:48:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json    
# Wed, 23 Apr 2025 14:48:05 GMT
LABEL "build-date"="2025-06-30T12:38:11" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="f6591f6fb99f567a57f1c8ac4572758f722a244a" "release"="1751286687"
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 23 Apr 2025 14:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 23 Apr 2025 14:48:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENV JAVA_VERSION=jdk-11.0.27+6
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='4decd2e5caf4667144091cf723458b14148dc990730b3ecb34bba5eb1aa4ad5d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.27_6.tar.gz';          ;;        ppc64le)          ESUM='9407ecef765ec681fb187f084f1e029001abd5baf7a13b32067e9cbdfb140130';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.27_6.tar.gz';          ;;        s390x)          ESUM='89df8583779b880f21b6cf29ddd9438961e2b1a092f416d05255fd6cd7f0e9fe';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.27_6.tar.gz';          ;;        x86_64)          ESUM='dc6136eaa8c1898cbf8973bb1e203e1f653f4c9166be0f5bebe0b02c5f3b5ae3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.27%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.27_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 23 Apr 2025 14:48:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 23 Apr 2025 14:48:05 GMT
CMD ["jshell"]
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:2129d80cee89f438c6dbd429ffb54a5978b65e615ac7fd433ec00fe2bade0ebd`  
		Last Modified: Mon, 30 Jun 2025 18:10:12 GMT  
		Size: 37.8 MB (37768278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e9aec8fd0e12be817de4d5fab94fc3d67321bd301387b7bdc8133dc34cf67d`  
		Last Modified: Wed, 02 Jul 2025 18:45:50 GMT  
		Size: 27.6 MB (27579669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed842500204f768f8c655e1d118c5a2947c9af22dc10122e684ffe4c91576066`  
		Last Modified: Wed, 02 Jul 2025 20:18:36 GMT  
		Size: 122.0 MB (121994622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cbec08be4c2029068566d92629b3de9a5e22f52ca0f1a46d69c3ab1f934935`  
		Last Modified: Wed, 02 Jul 2025 18:45:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3598bb18d10c6d852fc508adc98dc9941ade8c8e3eef4ff3272ed0fcf35f252e`  
		Last Modified: Wed, 02 Jul 2025 18:45:46 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ec3575ba7095e6734fa9818058813974f0ef35b11836fec8d9c42475b5690`  
		Last Modified: Wed, 02 Jul 2025 19:21:00 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901818f1462cd822ee7ce31927f5573e596c36f57c8b67c22c14813a43c2c3d1`  
		Last Modified: Wed, 02 Jul 2025 19:21:02 GMT  
		Size: 36.4 MB (36434725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f188ce185285ce1d860bdc9697ef862403ad123add997ac504181704dd20c3`  
		Last Modified: Wed, 02 Jul 2025 19:20:45 GMT  
		Size: 137.4 MB (137395488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d273f91a4802950a1c8e067851bf3431c8574eda6855d5db713fa1c0c4afed1`  
		Last Modified: Wed, 02 Jul 2025 19:20:59 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:fa1d0e44fa3448fd2d088d68dbcc42bafbfc2069ff723fbe5a98a7f546671127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5409188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e3d5f6d3b088e166c1730a4ec32cce68f60e0e6f651f03a7af35d813ab34c3`

```dockerfile
```

-	Layers:
	-	`sha256:2a704bfc79947c4c91db1a4911a23df294eda081099cb63e7e471806a4d3275e`  
		Last Modified: Wed, 02 Jul 2025 20:21:19 GMT  
		Size: 5.4 MB (5384910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c607073478d7551a84d6b9f050c6f29ba8a70bc38a03d5be3be6db83b6ab98`  
		Last Modified: Wed, 02 Jul 2025 20:21:20 GMT  
		Size: 24.3 KB (24278 bytes)  
		MIME: application/vnd.in-toto+json
