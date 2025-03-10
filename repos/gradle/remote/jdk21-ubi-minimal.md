## `gradle:jdk21-ubi-minimal`

```console
$ docker pull gradle@sha256:3ed0a0470c74e3d0f1ff518987e4c0d68385c9f8a9bd367f5e22d9128411934d
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

### `gradle:jdk21-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:0676620a5b2a36896a64a2518f5bc7a5e03f46c33dc3083ab0eb25bd776136d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.6 MB (406588489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473450dfb9a0e8d31df17ced65e00157af34ee636ccf3f1957ff04048367a61d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:a07d6464b408a07384eb87b8e371fb05260f293df1fdae9e20c1a6653e15e37b in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-03-10T09:47:15" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64le)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:ecb02bde81105b662eaf8da4b200f811c2ac8a0dd37e0c09f19de54603c5c8fb`  
		Last Modified: Mon, 10 Mar 2025 10:32:31 GMT  
		Size: 39.4 MB (39376539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92b0a09d78952dd6b3d60aa8a9f9ef1c8282b59a65bcc5aa506acb82686576`  
		Last Modified: Mon, 10 Mar 2025 10:32:31 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748937d1676139f8b56d7f982fb7ef3d19123b97786d011a5d4d9e5cca7bbaa1`  
		Last Modified: Mon, 10 Mar 2025 21:06:10 GMT  
		Size: 37.0 MB (36972923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e21263f5011ba4aaa878f8989c2f782f00d6990994e8d44edecd8f1a584d5f1`  
		Last Modified: Mon, 10 Mar 2025 21:06:13 GMT  
		Size: 157.6 MB (157590668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f477f3f0e65cdb7a6cd887f1349163da370773938611592c0c192084112292f0`  
		Last Modified: Mon, 10 Mar 2025 21:06:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ccc550f3f1567bfd53237f44443d137c23f24aee57ca282a71f502160d771a9`  
		Last Modified: Mon, 10 Mar 2025 21:06:09 GMT  
		Size: 2.3 KB (2287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adb13c6853fd702cacf8fb7f3bdff3eaa7ba610592f1d4b1db59826ce94e8ac`  
		Last Modified: Mon, 10 Mar 2025 22:11:20 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28619ca47b38e9766e95e9539885e4837b217abc50f9cd9742e89cfeab0c0b1`  
		Last Modified: Mon, 10 Mar 2025 22:11:21 GMT  
		Size: 35.6 MB (35600660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ac77723e4f829f7d2398f82afe16dde303138de1a1580780549882990bda8e`  
		Last Modified: Mon, 10 Mar 2025 22:11:22 GMT  
		Size: 137.0 MB (136988184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cd716eb49ddb30c4b56e089246a7cbaa5b17a3f56fe6982fe319f588859685`  
		Last Modified: Mon, 10 Mar 2025 22:11:20 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:c21747fb1ad1fc545a5b7209ececd74c4794f2ab846082ab83d61041a08c0925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6533513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e651a95b4bb831e5cb4b4c1d544558845cadc358388f96c1d4a271b150aa83`

```dockerfile
```

-	Layers:
	-	`sha256:e38c15368bbf7816e3d197d60f456575faca4ee8b83f2605e88a5d781566b950`  
		Last Modified: Mon, 10 Mar 2025 22:11:20 GMT  
		Size: 6.5 MB (6509752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb60a97de75f9930fd8e144b83af972aa306207a7d7c8a72dc3363fb87a31d4`  
		Last Modified: Mon, 10 Mar 2025 22:11:20 GMT  
		Size: 23.8 KB (23761 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:12ebce151471733a39d1a41fe3a645d19823af3d6e377ec3dfe975228829f3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (403014694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b8797af9e5eaecbb892139ebdf730a78b59912eb3c08f245bb730f8589f298`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:7cf9b7b9f60ce494e82504114b8e4e8497504001337c87ffc50d4a40fe4f9edc in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-03-10T09:50:07" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64le)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:f7b8fe7f82e9c2744a37d9d57d915bba00fe3879ae010a254770d6de52407d6b`  
		Last Modified: Mon, 10 Mar 2025 10:36:22 GMT  
		Size: 37.6 MB (37585537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b83df990133b9bdb95a233cede88e14a9e9f42d8a90daca3368a0795857bbf6`  
		Last Modified: Mon, 10 Mar 2025 10:36:20 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9ed2e900cb7085312fdb231cce5437b781a3044b7d2f27cc07d6e098d2d925`  
		Last Modified: Mon, 10 Mar 2025 21:19:31 GMT  
		Size: 37.4 MB (37433861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690a23eb2e3fbdfa496c5803c94b3cc8510b3316674e065f52e1ac4dfce7f00`  
		Last Modified: Mon, 10 Mar 2025 21:30:49 GMT  
		Size: 155.9 MB (155858834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7796ddc3ba53633f1ab4d32f2dfbd2bbeedf6925cdf99646e03ff4d75b24c88`  
		Last Modified: Mon, 10 Mar 2025 21:30:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779dae9454d69d758fe04d167d5ee671de2e7aba9dc83a6e8afc8a05ea1572c4`  
		Last Modified: Mon, 10 Mar 2025 21:30:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c97d13c1c19b7f22d25c20214f83653f8c2dd310d9ce73880cf5c58a443d60`  
		Last Modified: Mon, 10 Mar 2025 22:12:37 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ee6e22f1f9b00d844d6adfe22af9cb271386cf95b876ba45a3cfd88f8cc43e`  
		Last Modified: Mon, 10 Mar 2025 22:12:39 GMT  
		Size: 35.1 MB (35084132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce184feae6d8a71fc8fd6a8d4fdd192a2095da69811c1643fdf1ccf7a7ce7c6b`  
		Last Modified: Mon, 10 Mar 2025 22:12:41 GMT  
		Size: 137.0 MB (136988184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d13a6a8f9d66e8014d84e93b8121affa8d6c10276fb9184e9c85105b38808`  
		Last Modified: Mon, 10 Mar 2025 22:12:38 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:b7fa30b8259856721170de529f97e458ed0eab91ea3991749b13cca05f0a05d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6532965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ef412bfbe4c54cd3489c9c83d419cdd3d42d299e1e2522a1f55be9463c922f`

```dockerfile
```

-	Layers:
	-	`sha256:2fe68d5dbb2424074a6fbf1f22ae9234f2a773adb3d471c4694ceb15929713cf`  
		Last Modified: Mon, 10 Mar 2025 22:12:38 GMT  
		Size: 6.5 MB (6509007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7cfd7472b2b2d0681c60b956c466c1cf530f85f08a6ce65901c5a8436cff80`  
		Last Modified: Mon, 10 Mar 2025 22:12:37 GMT  
		Size: 24.0 KB (23958 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:3163ee82bf71f80379d8b47491d4e5be4e49a0eebad5bc0d98d6fff9a576f68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414829193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a0fa055483fa3ba34358aff39202855fab68916a9d2fa42da3e55191bd6ad2`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:da1ec7f34262056221a653ac74b71b17804f2abbdaaf0edf8f887dc2c1eeeb91 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-03-10T09:54:50" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64le)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:2ad90c0e47251160a30b1b70efa8a3c13ef0ce7a213f619f4ac82370a7ac2dae`  
		Last Modified: Mon, 10 Mar 2025 12:25:37 GMT  
		Size: 43.8 MB (43784081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4046f47b13f500df13fbbe4b00a43b66c2ff9fcbf6923a82edf7ae12f8ac46d9`  
		Last Modified: Mon, 10 Mar 2025 12:25:36 GMT  
		Size: 462.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cac67f3417b20c312f6f519732ea676adf524a26cd705e32535b9523e7a04a8`  
		Last Modified: Mon, 10 Mar 2025 21:07:28 GMT  
		Size: 39.5 MB (39465367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446847c5eb0cd1c049a2a7a689e59c642b5c4de750080a295297fa3c46905ba9`  
		Last Modified: Mon, 10 Mar 2025 21:49:19 GMT  
		Size: 157.7 MB (157745575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ad01f13e92948eccec11bee59b59052c05ed1ded05da959349acde4086c202`  
		Last Modified: Mon, 10 Mar 2025 21:49:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0437f88fcf505054bf247043316c5034bcee3018288e22b03305a5972d65457e`  
		Last Modified: Mon, 10 Mar 2025 21:49:15 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f38d6a17aa54052e3c39c2e6b58fbc117ecea52b5f712c8efaa4251a3b050bb`  
		Last Modified: Mon, 10 Mar 2025 22:11:48 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30d4c142455dd843a5b637c07da51f2006890a56bae14d3c00172e06fe62942`  
		Last Modified: Mon, 10 Mar 2025 22:11:50 GMT  
		Size: 36.8 MB (36806361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d172ba97e82e4dd3e005693a252f2c0eab05214a836d3d6925bab616498df83`  
		Last Modified: Mon, 10 Mar 2025 22:11:54 GMT  
		Size: 137.0 MB (136988184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbe77b709aa7b4404bda65c31a50c64de89fa042e73bdb0874b7bb296b31ae4`  
		Last Modified: Mon, 10 Mar 2025 22:11:49 GMT  
		Size: 35.0 KB (35002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:0729c4da456e29911bac6142b775851f427800577f18147682946d2ec0b5c9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6530747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1b979df34dc32bb6d5ada3dde6964f564f666ed9c875dec6bfc74bd27caeb5`

```dockerfile
```

-	Layers:
	-	`sha256:aaa41dcd614cd567593c1f3b0195ea6088649bb7133aadf708194050a8dad230`  
		Last Modified: Mon, 10 Mar 2025 22:11:49 GMT  
		Size: 6.5 MB (6506912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fe27a1308f8c70dce5cd613f18339461e1f6ced4d97b8128de64d5022d716ab`  
		Last Modified: Mon, 10 Mar 2025 22:11:48 GMT  
		Size: 23.8 KB (23835 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi-minimal` - linux; s390x

```console
$ docker pull gradle@sha256:26766ce66f57a83b7b947a25f0813b947945714c9f9abaf521d76eb48bc949e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.7 MB (393681295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b1bade9825532d7a21f95d4ce1830e701f344e7edd6499bba4295d747da3fc`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL url="https://www.redhat.com"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.5"       distribution-scope="public"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.expose-services=""
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 30 Jan 2025 14:32:57 GMT
ENV container oci
# Thu, 30 Jan 2025 14:32:57 GMT
COPY dir:03a99625d811dfe52ab91eb1e2d9bde6f2635b5ecea85281c88b7104fd8fc9f2 in / 
# Thu, 30 Jan 2025 14:32:57 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["/bin/bash"]
# Thu, 30 Jan 2025 14:32:57 GMT
RUN . /cachi2/cachi2.env &&     rm -rf /var/log/*
# Thu, 30 Jan 2025 14:32:57 GMT
LABEL "build-date"="2025-03-10T09:50:03" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="2f8e6c4d7ad22789d5663bf4bd66603301fba889" "build-date"="2025-03-10T09:43:12Z" "release"="1741599792"
# Thu, 30 Jan 2025 14:32:57 GMT
RUN /bin/sh
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Jan 2025 14:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Jan 2025 14:32:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='04fe1273f624187d927f1b466e8cdb630d70786db07bee7599bfa5153060afd3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.6_7.tar.gz';          ;;        ppc64le)          ESUM='163724b70b86d5a8461f85092165a9cc5a098ed900fee90d1b0c0be9607ae3d2';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.6_7.tar.gz';          ;;        s390x)          ESUM='5ba742c87d48fcf564def56812699f6499a1cfd3535ae43286e94e74b8165faf';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.6_7.tar.gz';          ;;        x86_64)          ESUM='a2650fba422283fbed20d936ce5d2a52906a5414ec17b2f7676dddb87201dbae';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.6_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 30 Jan 2025 14:32:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 30 Jan 2025 14:32:57 GMT
CMD ["jshell"]
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && microdnf install -y         findutils                 unzip         wget         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:9f806440d1e665fa608505f763022c8e47b2f9e29ccfb38f0816ce15a450c4b9`  
		Last Modified: Mon, 10 Mar 2025 12:25:32 GMT  
		Size: 37.5 MB (37537281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf806b0d10a5106a3d4d54aa3f736209953daa8a47543d90b3c7592b486b3a9d`  
		Last Modified: Mon, 10 Mar 2025 12:25:31 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c11278015e2c5e6c8a2a1a8cb610afa93aa48eee24370f07d67511201482918`  
		Last Modified: Mon, 10 Mar 2025 21:07:42 GMT  
		Size: 37.0 MB (36990976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43be0b09dd708b7374434f4fb09abac708e44e4beefc0d80bdfb75f52f1744f3`  
		Last Modified: Mon, 10 Mar 2025 21:26:22 GMT  
		Size: 146.9 MB (146858633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540193d8c0e52c7fbed2071d9d93a8570e765636f070f93c113bfe70100afae9`  
		Last Modified: Mon, 10 Mar 2025 21:26:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e334ad60e9525a5b8bf7c7259e6ee688816e1ea33646f81be4b495eff59cae47`  
		Last Modified: Mon, 10 Mar 2025 21:26:20 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2448a30a7024b0f9bfd8ab2ccb99a42ea3be27de7b8d977d9c7ca84b8eb6e3a`  
		Last Modified: Mon, 10 Mar 2025 22:12:15 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e901e2e3c04757430041b5df55bfbe946975eca10e67a6ef2aa968edde45cc`  
		Last Modified: Mon, 10 Mar 2025 22:12:16 GMT  
		Size: 35.3 MB (35266598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4f019186f7fba0a3176e09a70b4e900d54556d187f6e7b3995d0b581dc8c7e`  
		Last Modified: Mon, 10 Mar 2025 22:12:18 GMT  
		Size: 137.0 MB (136988184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1190023212cf450c86ec91a1f44d095304fcec4455f475538cbfaab6d006d259`  
		Last Modified: Mon, 10 Mar 2025 22:12:15 GMT  
		Size: 35.0 KB (35006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:c55a0fca11a58fe58e1765a359194accd4ec12fff1f22b46d4ae3e66975b2be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6519942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8014e906f1b2cc5546aa1622a0c4f1c54b358ced109397246df7d011c33b82b0`

```dockerfile
```

-	Layers:
	-	`sha256:ea6fcb57edd803a01b2951ccb95c8bec1736c23f95e0c5c2da6a3fffcedd5c17`  
		Last Modified: Mon, 10 Mar 2025 22:12:15 GMT  
		Size: 6.5 MB (6496182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402f27ebbb1dec26456fc0f8dc2b8ef6d5b87bb7a143ba180be608cbe834f3a8`  
		Last Modified: Mon, 10 Mar 2025 22:12:15 GMT  
		Size: 23.8 KB (23760 bytes)  
		MIME: application/vnd.in-toto+json
