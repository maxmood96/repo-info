## `gradle:9-jdk24-ubi-minimal`

```console
$ docker pull gradle@sha256:395d183d0f6d3323b0cd1e73e36273dcf2905c53f4145bd8218d5c2e9d0b54e7
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

### `gradle:9-jdk24-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:548c5af3da0cb7ef74047ec89579f70fa860e0c50b120a291ac6427a38ca3702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328494732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5e3c89394930af539a0281025e7157c9053becf5acc8cbd0708e1457266777`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.openshift.expose-services=""
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV container oci
# Thu, 31 Jul 2025 17:27:11 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["jshell"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311fc11b3192d1e0c2503786df212b28bc93927f3bd7fba31eea96288a63e451`  
		Last Modified: Thu, 21 Aug 2025 18:56:49 GMT  
		Size: 27.5 MB (27535996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48af9839e86f6570aa39972b85db9d0ec889fd2f883678934dfd7a5a32f47595`  
		Last Modified: Thu, 21 Aug 2025 18:56:53 GMT  
		Size: 90.0 MB (89974223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0da2fb4c268767bec017aad5fd34e88393c64ebe1d513ce6d291f83ec258da`  
		Last Modified: Thu, 21 Aug 2025 18:56:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba1904e24653ab07ce7412b2a17ebdec2aca8eab4d364c60bcdf18e85897cf8`  
		Last Modified: Thu, 21 Aug 2025 18:56:17 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1175f274b59914857499053af70114375f1fe5cdb74aad493760cc0aa79022f2`  
		Last Modified: Thu, 21 Aug 2025 19:09:13 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f78bab1c886155069c3ae1508dc228d70b0c68f7f8a7b546c931a37f859382`  
		Last Modified: Thu, 21 Aug 2025 19:09:13 GMT  
		Size: 36.8 MB (36797327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f63a4af47a903d4c2d61e412c5e464062fbc93f14bfd02200212d5d26495f9e`  
		Last Modified: Thu, 21 Aug 2025 21:07:37 GMT  
		Size: 134.5 MB (134480830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f058d204605b632e938aacaee90d73524150983b6a29d42bc9c4f4514da61`  
		Last Modified: Thu, 21 Aug 2025 19:09:09 GMT  
		Size: 54.9 KB (54913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:ef14f8b5ee7df5e3cac7575f637eb4e7451fc7cc7308be19210155012d7fc5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ace140376762477908482a14ab80e8a69f2ee5c7fd4432dd8ba81e5237af01`

```dockerfile
```

-	Layers:
	-	`sha256:87569aae8a81b0e5d5dd7c144a3dec5e9989b916cb45491959d80ccab89a768e`  
		Last Modified: Thu, 21 Aug 2025 20:25:10 GMT  
		Size: 5.3 MB (5325588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bec1487a657248e4670baa6e753c212a79cb26f4c5beedd9b591f0861eda042`  
		Last Modified: Thu, 21 Aug 2025 20:25:11 GMT  
		Size: 24.2 KB (24246 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk24-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cde4e8ab14d161ce3e5ed2d3834bc940131cd8b126ba09b3b770443ff9c31ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325734172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc4ce6fbcc030c5137788cc761fff892f21cac0bf3f2c54623b8d1266a274f6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.openshift.expose-services=""
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV container oci
# Thu, 31 Jul 2025 17:27:11 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["jshell"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e17f845c350df4a3ae23fd2059cb6d4648e286464721512126cbcada0851f56`  
		Last Modified: Thu, 21 Aug 2025 21:07:30 GMT  
		Size: 28.0 MB (27983377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba6e2afafb8213962960975980343d000399b2601608d10ed5858f7e299561a`  
		Last Modified: Thu, 21 Aug 2025 19:07:58 GMT  
		Size: 89.1 MB (89100525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb6632a7c82fb54bd5227d485a4c9a42e6012e156d496b2911036298eb00f5f`  
		Last Modified: Thu, 21 Aug 2025 19:07:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eae20f0b1e7b695788d57fc91b96e9512ed1b609bcb368561632b8fa080b9ab`  
		Last Modified: Thu, 21 Aug 2025 19:07:51 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05038cef525c76943618dccee0653f5440326dfa60e5d54c0cffcb3f3e0598ca`  
		Last Modified: Thu, 21 Aug 2025 20:03:00 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8759184a3398d153bc5c4ae0ddc8b671405816055aa338094b765586c81bc058`  
		Last Modified: Thu, 21 Aug 2025 20:03:05 GMT  
		Size: 36.2 MB (36246164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029563f0b03af4378e0a62713e65364494a3660ad1d1f92547ee2c784ea47973`  
		Last Modified: Thu, 21 Aug 2025 21:07:39 GMT  
		Size: 134.5 MB (134480834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3e99a4bdcad7dd07a70b84ac0765050b6b4caae8b85bf8cf9d72e9de0c5a1b`  
		Last Modified: Thu, 21 Aug 2025 20:03:01 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:78cf718090c925b641df5f73ffc1dd8d87c3958ab92ee85ed74e69d040317117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b0e47b8ece8bdbf24013387e267cf8d4f0b6bde871d7d0b60360691af769e0`

```dockerfile
```

-	Layers:
	-	`sha256:5e3af8eacbf02966184d305f04616c475b34f9683ac7ee573817f4a20cf98f4d`  
		Last Modified: Thu, 21 Aug 2025 20:25:17 GMT  
		Size: 5.3 MB (5325017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a383e2fbb3e3bfe882823370974e4a6efeda048a57c8879f6be9a5485daa5643`  
		Last Modified: Thu, 21 Aug 2025 20:25:19 GMT  
		Size: 24.4 KB (24443 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk24-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:2e8c415409b8e8cda632b30ec02b3b177b830e4b535e54dce1b7c7395f418d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336605431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27141207e6cd459913978ca4c3fa17f8dcc4659c91954a8d229e809be9eb311b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.openshift.expose-services=""
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV container oci
# Thu, 31 Jul 2025 17:27:11 GMT
COPY dir:d2207f84596636cf1f42082a4111b6c38656ec970ae8b2e1ce2cacd7d29f1510 in / 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL "build-date"="2025-08-20T13:11:42" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["jshell"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
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
	-	`sha256:b47ae6a8841c8c80b698da50154046aadba3c0dacc3a01bbd4dec94c5874748f`  
		Last Modified: Thu, 21 Aug 2025 19:12:58 GMT  
		Size: 89.9 MB (89925034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e4272ad432728ee97f183fca1457a0bea75b2c825574f653ef58a205126b87`  
		Last Modified: Thu, 21 Aug 2025 19:13:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eba3a5891e4721fce130ee1ec4f2e7d2a84dc078af4e760ccae7742827e735e`  
		Last Modified: Thu, 21 Aug 2025 19:13:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd1a679f1fa54d0db2af6eb91aed2c069e4c8bdad7747f00245fb129d2c5704`  
		Last Modified: Thu, 21 Aug 2025 19:57:53 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a6be0defdae5d52bc909a1eec3e3644a2bad40917527a255791c33d8209260`  
		Last Modified: Thu, 21 Aug 2025 19:57:57 GMT  
		Size: 38.1 MB (38125522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234cad55997e764436800794c61e2bd474e1201b19466c9aff567a44845d820`  
		Last Modified: Thu, 21 Aug 2025 19:57:36 GMT  
		Size: 134.5 MB (134480840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376f50b88fdb2ba758bd4a114c102bc31b462d02644f0af52c9f3746c6b2148b`  
		Last Modified: Thu, 21 Aug 2025 19:57:52 GMT  
		Size: 35.0 KB (35015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:fb9bd6f69a2618ebad53012ee9772f8a142fff565152c2b6dad7dc8470853f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbdb4ef24ebda2b403c26e092b2a319c484a94e45b5332222c3aa7f4b2b4e8b`

```dockerfile
```

-	Layers:
	-	`sha256:ff7845268a4a8e4bae734b4e97e968bec97aa0baaece8092986ccd29faf2443b`  
		Last Modified: Thu, 21 Aug 2025 20:25:25 GMT  
		Size: 5.3 MB (5324223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b58e003f6200858d31c4ea6c512acbef2e900f3b631d15da10d46bd540a6f74`  
		Last Modified: Thu, 21 Aug 2025 20:25:25 GMT  
		Size: 24.3 KB (24320 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk24-ubi-minimal` - linux; s390x

```console
$ docker pull gradle@sha256:541df525b4f26a3be029d1b26526923738fd1273fa496ac1df9c8060668e1f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321494151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565d1f79f5fd9cff4ce5b3a4b1b1482fc042329270e360fe12b2da8394f475df`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.openshift.expose-services=""
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV container oci
# Thu, 31 Jul 2025 17:27:11 GMT
COPY dir:81aabc5a8685d8fef8565a119a36f85579c02d5407baf6eca1107100bb225623 in / 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL "build-date"="2025-08-07T16:43:10" "architecture"="s390x" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='6f8725d186d05c627176db9c46c732a6ef3ba41d9e9b3775c4727fc8ac642bb2';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_aarch64_linux_hotspot_24.0.2_12.tar.gz';          ;;        ppc64le)          ESUM='00f55805b4fa34c2557428e7f43ac847a8af0177ecb0b9dd8a6016f313ec43a9';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_ppc64le_linux_hotspot_24.0.2_12.tar.gz';          ;;        s390x)          ESUM='555059f4929ab6435eb83b496d0b969bc6a9a5c07915d5f7607f5d833e38fb39';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_s390x_linux_hotspot_24.0.2_12.tar.gz';          ;;        x86_64)          ESUM='aea1cc55e51cf651c85f2f00ad021603fe269c4bb6493fa97a321ad770c9b096';          BINARY_URL='https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.2%2B12/OpenJDK24U-jdk_x64_linux_hotspot_24.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["jshell"]
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
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
	-	`sha256:2265656267968c56f6aa8133b196577e3b056d89baedc14e90bfd26c441e1471`  
		Last Modified: Fri, 15 Aug 2025 04:46:57 GMT  
		Size: 85.2 MB (85226359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64ef3435de4650f2b53735a28e627d22a54a7f96d460b0a53fce1c126208326`  
		Last Modified: Thu, 14 Aug 2025 04:44:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20088aa4215f997f1bd080489fdaccd66c355b5ec7c432b6d74feff4e7d9ca46`  
		Last Modified: Thu, 14 Aug 2025 04:44:10 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047d2208374a8641e810b132bb2963c436ccb418acc7bb6544f9573c53511e20`  
		Last Modified: Thu, 14 Aug 2025 10:49:56 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abf4a5378f5e4a4c0767a7e106eeec359072a9e46522c6d454a7669393619b4`  
		Last Modified: Thu, 14 Aug 2025 10:50:07 GMT  
		Size: 36.4 MB (36429451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c7c3dd76e97764b306c277c25faec7b7e40e158bbeda0b50da01868efbcfa5`  
		Last Modified: Thu, 21 Aug 2025 01:24:00 GMT  
		Size: 134.5 MB (134480837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79966478accbc975c63e8a27fbdf46dddd11e340cbbdb9390da221850216c4c0`  
		Last Modified: Thu, 14 Aug 2025 10:49:56 GMT  
		Size: 35.0 KB (35017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk24-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:17f1b74e89e690a7d33c48a93e46b06f94cf7de48098b38e534e9da6f752c44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ab3b09825be7a5ee2f7e72644374c86104563b4d13e36b41c1f5df1beeda13`

```dockerfile
```

-	Layers:
	-	`sha256:5ce42796cb8d3ae95748065a58e0e9e92b73b7ea3af12c585cf586953c40f6b6`  
		Last Modified: Thu, 14 Aug 2025 11:23:44 GMT  
		Size: 5.3 MB (5314743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc6fe369b7db373904cef0c471ade55df9e02e370ad39810c83cf87b652a9062`  
		Last Modified: Thu, 14 Aug 2025 11:23:45 GMT  
		Size: 24.3 KB (24262 bytes)  
		MIME: application/vnd.in-toto+json
