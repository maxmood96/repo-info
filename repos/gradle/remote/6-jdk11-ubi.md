## `gradle:6-jdk11-ubi`

```console
$ docker pull gradle@sha256:3998ed3d308f63a74b38cfaaf8fe5f40d99c2578fc3eed4ffd03a297f0b58cec
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
$ docker pull gradle@sha256:b950fee3d558ad20ca20d171de0382d8ea472151ea5fea0d78a6158c0bf61d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354231068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14adc4908fbfa0bcd92ecb462a039472aa587e6d0f44b3035f6de0c5921fbfce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 02 Jun 2025 18:02:05 GMT
ENV container oci
# Mon, 02 Jun 2025 18:02:05 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Jun 2025 18:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 18:02:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["jshell"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094fc607a903b67a99cbd4f59b8fad40f27c8ba2a410528b194d92144baf860a`  
		Last Modified: Thu, 21 Aug 2025 18:56:03 GMT  
		Size: 27.5 MB (27536459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068a5458fdec437a6738728e4c3bd468cd9f86d58e69156a694e8f408b1489b9`  
		Last Modified: Thu, 21 Aug 2025 19:08:27 GMT  
		Size: 142.1 MB (142117865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed86878ed0c342cbeb74a91639bb925bdc11ccdf547f0b62448e6d34c2665381`  
		Last Modified: Thu, 21 Aug 2025 18:55:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85b4a524b23756efb8c7b8f533475b41de50e49caedcede15fc5839e20900fb`  
		Last Modified: Thu, 21 Aug 2025 19:08:08 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c30ed3d82f4c31ea88f7694c4124f5becad98fa531cb4c23ccd36fe35a631e4`  
		Last Modified: Thu, 21 Aug 2025 19:10:59 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e04e0afcf4c36920c56b741c43b723fba28673596d2cdc44e43bfe7296a3dc`  
		Last Modified: Thu, 21 Aug 2025 19:09:00 GMT  
		Size: 36.8 MB (36797371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04e906f4d7ef0f79b3fd0bfa31e320929ba449d17550dbdc89837578cd3974c`  
		Last Modified: Thu, 21 Aug 2025 19:09:01 GMT  
		Size: 107.7 MB (107696650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aeeb2a466a54a372b28e7ce6215a8aebbc9be8d3a87e93831e0ba29cf8bf87`  
		Last Modified: Thu, 21 Aug 2025 19:11:04 GMT  
		Size: 431.3 KB (431280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:f270743d6daf2d690e7ad30628114b2d0cb0662413c3ffd177a3d7dcc2cf5636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5324003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d36d602a75524315d834071131a9f2a4d973f0c6f9f265a7fbf1fc4fa1c045d`

```dockerfile
```

-	Layers:
	-	`sha256:516cd763e83a8f65ba0949783f07b6e735953b8873814aa4a0d0510f31c2de43`  
		Last Modified: Thu, 21 Aug 2025 20:17:35 GMT  
		Size: 5.3 MB (5300374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2f62b7df86df81702324b8f131183666770e792009111c9dc0af0d302ba1dab`  
		Last Modified: Thu, 21 Aug 2025 20:17:36 GMT  
		Size: 23.6 KB (23629 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ae46a10d57cbd3d2fe74c2ad58bceb6aeb9e12f253de24f5b97a2cb21f851c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349100038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0016602f8b3bc0b7d75df9ad1098ec512175e7f0ffdea22e3ef5da08c910ff3e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 02 Jun 2025 18:02:05 GMT
ENV container oci
# Mon, 02 Jun 2025 18:02:05 GMT
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Jun 2025 18:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 18:02:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["jshell"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:ae68ff313f78851fbf66137c0a49a327986447045fa7f2497adbc1b57f88db56`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.8 MB (37819116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52d35c18e9a72456397f9eeedbd19f9dc8600f65f4d8fd5d96621d533551288`  
		Last Modified: Thu, 14 Aug 2025 09:09:50 GMT  
		Size: 28.0 MB (27982673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772b21831ddbbd852c6aad1dc50c0542e4431177de5fd5904e4895ce37e55137`  
		Last Modified: Thu, 14 Aug 2025 12:19:40 GMT  
		Size: 138.9 MB (138923679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bb617948aea5534c3d27a4001a8b354ce6349dad463d5d0d70300b19f4470e`  
		Last Modified: Thu, 14 Aug 2025 09:11:53 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e74742d3f1972af3ebfdd935b631774f08a2448acf4e6de4e974f464a1578d27`  
		Last Modified: Thu, 14 Aug 2025 09:11:53 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330557d96b0bd9268b61b99d7f5b15096ad47d296dc8e1f1d45dcb3aad26540f`  
		Last Modified: Thu, 14 Aug 2025 17:23:34 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6adc0cb6ce6a04c00872fcd12a965680838984a330ce119cfb58674cfd01a1`  
		Last Modified: Thu, 14 Aug 2025 17:23:53 GMT  
		Size: 36.2 MB (36248745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47a77d8b01afac5684b339b59e773a4fc3eaea1fa06bed487aa9478a9538f30`  
		Last Modified: Fri, 15 Aug 2025 01:35:19 GMT  
		Size: 107.7 MB (107696653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3d1add8f195d6e223861d0a46cd7d2e2bd2913a41d2a7185d697fa1fabc681`  
		Last Modified: Thu, 14 Aug 2025 17:27:10 GMT  
		Size: 425.0 KB (425015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:57b17c6f5d2948af04029cfc0c307d471431faf948d43da76c15fe13da08c73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5324202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c582453e7a8f894ab9576afe84d4cf6aeacfbecb2f394fb6150eb5d02cbad3c`

```dockerfile
```

-	Layers:
	-	`sha256:2ed1fddfc4921d1e7668e5c88de8c4c668c1fd950cdf5f471ada33c1472f0d4c`  
		Last Modified: Thu, 14 Aug 2025 20:17:38 GMT  
		Size: 5.3 MB (5300400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e571f186e25f773ebc7c8fd7944c2414d758d185a335d9e1410309bcbc97dbb`  
		Last Modified: Thu, 14 Aug 2025 20:17:39 GMT  
		Size: 23.8 KB (23802 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:8e0c69624a4245a62f04660d5d82d60425423ab19e90600b06553630aeee69f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349252873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8696410d367748a9d1e5a6315e5d61b55df0620f965c59e6fd55902617541c9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 02 Jun 2025 18:02:05 GMT
ENV container oci
# Mon, 02 Jun 2025 18:02:05 GMT
COPY dir:d2207f84596636cf1f42082a4111b6c38656ec970ae8b2e1ce2cacd7d29f1510 in / 
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL "build-date"="2025-08-20T13:11:42" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Jun 2025 18:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 18:02:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["jshell"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:ebd7c9ee3cc0108f33ad80f84c3da96a78c10cc76b3dfe38b2b8ab879a83a307`  
		Last Modified: Wed, 20 Aug 2025 18:13:19 GMT  
		Size: 44.1 MB (44057494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9b8d104c4d92c5fde801246053d3fe5d18514fbdb85ec097aafc6d73271add`  
		Last Modified: Thu, 21 Aug 2025 18:58:27 GMT  
		Size: 30.0 MB (29977366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642815719b1c3a83dade204b3f9b2e56294311354ce9169ff3735d8c547cf75f`  
		Last Modified: Thu, 21 Aug 2025 21:58:13 GMT  
		Size: 129.4 MB (129356802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26086e8bdadce9e50085d45606e9ae2f37c7f42c15d6d9753ecb486578b10bb8`  
		Last Modified: Thu, 21 Aug 2025 19:01:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28ae41a4b58e013a32e5fbdd5325f47da9bd694752b754ccdc688eef5a7feda`  
		Last Modified: Thu, 21 Aug 2025 19:01:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ac7f5fd1d129397124f2e31da421d8779169cc61dfef661f4b635564d610d`  
		Last Modified: Thu, 21 Aug 2025 19:32:18 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2cd29f94d6c11e9bb9950f6a1bd5fa0dd608c49235011edfc930912389a400`  
		Last Modified: Thu, 21 Aug 2025 19:32:22 GMT  
		Size: 38.1 MB (38125393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e399612caff92be4ae094f798c12309b9784f33adc6d0a077b0e9a778f6587cd`  
		Last Modified: Thu, 21 Aug 2025 19:37:51 GMT  
		Size: 107.7 MB (107696674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1ea082340502a57ade868e080c75bbc028dbb2001771400735cd0413349f35`  
		Last Modified: Thu, 21 Aug 2025 19:37:41 GMT  
		Size: 35.0 KB (34983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:781f78c9704b0e52b1185a000769593861040ef77081667d4f019e654d3dd9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5320774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d4f4325243d4dc6106be418c7b19e71c933d3f4f3fc93ec788f1d494b938f3`

```dockerfile
```

-	Layers:
	-	`sha256:1ae7d02e6d9b4d70c5bd9f0b8781bf041acb7f9cfccd9b745b00653d596b8642`  
		Last Modified: Thu, 21 Aug 2025 20:17:47 GMT  
		Size: 5.3 MB (5297084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2e27e8cb88653f6d2ff70bfc2197682cb90d8fa84fa1ee8d11892a26a21363`  
		Last Modified: Thu, 21 Aug 2025 20:17:48 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:267821de840494a3ca9290d0e16a421ddcfa606146dbd0f0807bd74b31b877ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331513954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21095c28926802146774257224e960023c2dd0a23def3e9b857372895d994349`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.openshift.expose-services=""
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 02 Jun 2025 18:02:05 GMT
ENV container oci
# Mon, 02 Jun 2025 18:02:05 GMT
COPY dir:81aabc5a8685d8fef8565a119a36f85579c02d5407baf6eca1107100bb225623 in / 
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:02:05 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Mon, 02 Jun 2025 18:02:05 GMT
LABEL "build-date"="2025-08-07T16:43:10" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Jun 2025 18:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Jun 2025 18:02:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='32c316cb3998a9c9dee2829fbb577ea1c0ed666700cec73e049d44c342bb19af';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.28_6.tar.gz';          ;;        ppc64le)          ESUM='e272abd162b3de68093630929453feba3e63a5ab1bbb912379f6a4aa968ef06a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.28_6.tar.gz';          ;;        s390x)          ESUM='ac3f94fdcc5372e90f44fad9cd03ec0e3fd3535fea06c120f85e4a7534c6de04';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.28_6.tar.gz';          ;;        x86_64)          ESUM='7dfd551795a8884b26cbb02e0301da95db40160bb194f48271dc2ef9367f50c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jdk_x64_linux_hotspot_11.0.28_6.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["jshell"]
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:9712950bf0e31a37c30913225021f463d7b22862e610e77091d25d700d4d3267`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.7 MB (37742078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d75ef921e7de3e981a3faf28304d557974df7259d88d93abe80a3e9fdd66a0`  
		Last Modified: Thu, 14 Aug 2025 04:00:48 GMT  
		Size: 27.6 MB (27576245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602e05fecab17f416731267b35e832665857f611a86158e10b5bf69a63b21e0b`  
		Last Modified: Thu, 14 Aug 2025 06:13:44 GMT  
		Size: 122.0 MB (122030641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988dae11f18c3cfeb17cad24c3ca14242398a2140f7e6dc190761545aa9a014c`  
		Last Modified: Thu, 14 Aug 2025 04:00:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d3eb8b459c69921d8eff69b22253478bd2e8e984a3a4ee588239f6ba9d4efc`  
		Last Modified: Thu, 14 Aug 2025 04:00:42 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daaba9f402746caddb0fb6772f38348b3e575e4b69daf98f3433b399d802336e`  
		Last Modified: Thu, 14 Aug 2025 11:08:57 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3631215d55a3325ce4beaefcac6c402ea1fb21da8dd033f51116bb3e87766ca4`  
		Last Modified: Fri, 15 Aug 2025 17:53:28 GMT  
		Size: 36.4 MB (36429189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6cca497b976163dba0958e5b34869eb64d42151e4aa576697fe4eb4fdf7f542`  
		Last Modified: Fri, 15 Aug 2025 17:57:16 GMT  
		Size: 107.7 MB (107696654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1b450e21bc808cd76a5b1e1e3d2682a3fc8349306c8ec161b59bd2f3f49078`  
		Last Modified: Thu, 14 Aug 2025 11:02:03 GMT  
		Size: 35.0 KB (34987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:47e9b3c4c7157446099eac50667be054e16173ea0b57e5750f2d811af83133ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5310629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a03372a28a840ff4fc1346ef0f9872ff9253acc4d6ba5281ac08ba9fd91d3b4`

```dockerfile
```

-	Layers:
	-	`sha256:9e23aa4538cf68ca0a948afe84aa09d6668f1d06f128797cfe51210550e20f7d`  
		Last Modified: Thu, 14 Aug 2025 11:17:38 GMT  
		Size: 5.3 MB (5286985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37329c935f1187b04ba3c30f29b6041a81f8ae3bb211366007c79cbab733c8ad`  
		Last Modified: Thu, 14 Aug 2025 11:17:39 GMT  
		Size: 23.6 KB (23644 bytes)  
		MIME: application/vnd.in-toto+json
