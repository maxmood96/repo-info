## `gradle:6-jdk8-ubi`

```console
$ docker pull gradle@sha256:8fc811ccebefdc3d46490f4f4d640cd43c1f570b1b4c3b735ac51e93083b18a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:6-jdk8-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:d1831f830e1b693c29fb8ab4b31d3257130005d7cc004945fc2bbd52bb124b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266844926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4b7f6f542a2d8c8c39bb5d7cfc7d48416d9311542ac3f68414ccbec65ed5d6`
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
ENV JAVA_VERSION=jdk8u462-b08
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:c3fc299f9ba8af9e257cda11a9d33ae0268431773bb3bdde508b22b901e03b13`  
		Last Modified: Thu, 21 Aug 2025 18:55:46 GMT  
		Size: 27.5 MB (27536143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661d497d2daf98818d6f17f61cec3d843ef4020c7f558f75ec93335a9ef91229`  
		Last Modified: Thu, 21 Aug 2025 18:55:50 GMT  
		Size: 54.7 MB (54731902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c4a0517158da104a19359343abd18a3ad05d857ad4bc0050c64c4bb6c7095b`  
		Last Modified: Thu, 21 Aug 2025 18:55:43 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac6305887e3b6077824c25d702abbe94a5dfe5d1e52da23fe61f781a08bee0a`  
		Last Modified: Thu, 21 Aug 2025 18:55:44 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd58d6af34868f99b10199bd908a58f46f95fd02103e023ed4a1ab38f768a013`  
		Last Modified: Thu, 21 Aug 2025 19:09:09 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3c9172ddca2da4c9156a0570956a62649d92cab49e9bb630fc8ee30f7e034b`  
		Last Modified: Thu, 21 Aug 2025 19:09:16 GMT  
		Size: 36.8 MB (36797475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9a856ef8f3d7a3fcfa2cd41a52a38ae23f87b1c609b4a0524b11e70417b38d`  
		Last Modified: Thu, 21 Aug 2025 19:09:27 GMT  
		Size: 107.7 MB (107696668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc55e77a7c92913f3c472e059ac0989bbd5d6a1d03a1b545b9034f49d667571`  
		Last Modified: Thu, 21 Aug 2025 19:09:10 GMT  
		Size: 431.3 KB (431268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:4b6e1646dc5b0f8ef6ed08082d6adb3fbc0271edbd1ecba2dac89b1f49a7b7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25706ae4dfe1b264dc8784a6a59d9e2b6bbed68d764b05cfec1b9951fa47fe4b`

```dockerfile
```

-	Layers:
	-	`sha256:86d2e0e027edbe62b4e86adb2e28d7bbb63528517c9d3b002afe4a050734dcb8`  
		Last Modified: Thu, 21 Aug 2025 20:17:46 GMT  
		Size: 5.4 MB (5402462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b7f88601a1fdca8890aec623101a42377ffd1bd08e2616681c2df5ad163d372`  
		Last Modified: Thu, 21 Aug 2025 20:17:47 GMT  
		Size: 23.6 KB (23604 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fa85d86b18f1806fcc183b4050e9ba9bb9a0b0b104da4586ac048fc986dccbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.0 MB (264012776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fa0a5794aa9e4851d01ea61666bc1467a324da8f3485730dbdf370734b89a5`
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
ENV JAVA_VERSION=jdk8u462-b08
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:a5de5f4ef29624061ec40dd770b8babd1ac6e1fef85fdaf5c3283a9d51f55ba2`  
		Last Modified: Thu, 14 Aug 2025 09:10:06 GMT  
		Size: 53.8 MB (53836163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9709274f80fc47ec22d5e5e053b148acdcb6a9a801b29d6f59ff375d6ebbca`  
		Last Modified: Thu, 14 Aug 2025 09:09:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f5e1e1f890b9deb9c120ec4242b31616e519c9a0b310182abbbf6ebeac502b`  
		Last Modified: Thu, 14 Aug 2025 09:09:44 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9556017ac0cef767123dc225127daad16da3f6b9705d329b0d2ec689a12aec`  
		Last Modified: Thu, 14 Aug 2025 17:32:55 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dad1ab5d1278bf9c5464018e46322aad82974e8f03b0d8f7c2cbf2f60f09182`  
		Last Modified: Fri, 15 Aug 2025 00:01:28 GMT  
		Size: 36.2 MB (36248957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db011ec65de377f8a00af70f0a2c7d38852f7f0701daee0c166477aece8add58`  
		Last Modified: Fri, 15 Aug 2025 01:29:09 GMT  
		Size: 107.7 MB (107696667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9afe286d33a04b8c3922dfa39620724006c68fecc518d75c01a6f5e93d84d59`  
		Last Modified: Thu, 14 Aug 2025 17:27:46 GMT  
		Size: 425.0 KB (425019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:952df3a136ae957137062a38feeb52ae57d59cad30a1603ce075515008971c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290af9c6795745653bc69877c9ee7ab3bb1722c7005d8d6bd015a48d4146372b`

```dockerfile
```

-	Layers:
	-	`sha256:8acc8d367c725fc07548168d1438520963bcb5f587f2a60e49743e1a50d29a14`  
		Last Modified: Thu, 14 Aug 2025 20:17:53 GMT  
		Size: 5.4 MB (5402568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb6d732b9d5ef993735853a08caaafed9aebbef3661bd0494481016762acc1e6`  
		Last Modified: Thu, 14 Aug 2025 20:17:54 GMT  
		Size: 23.8 KB (23777 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:0f5f29911430f2546bbee6cf03ce0f8007fb8e05d0bd75fb753f6d8e5cc26b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.1 MB (272062104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9a2526e6846db0c91edb08c1a0d18b9a6dc5bc74dd935819fb334474f4e5ef`
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
ENV JAVA_VERSION=jdk8u462-b08
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
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
	-	`sha256:45b39f1b0a464ef4fe4cb0c1a7b93feabcbade1e0e63b08f41ae89015678c17f`  
		Last Modified: Thu, 21 Aug 2025 18:58:24 GMT  
		Size: 52.2 MB (52165988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc10cbfe25c3663243f96372cd81532973338e92366aa153e9b40351b02f00`  
		Last Modified: Thu, 21 Aug 2025 18:58:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f5a3db82c809f18b027511fd040e839c102b12b5103032d1c3c1344d033710`  
		Last Modified: Thu, 21 Aug 2025 18:58:23 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5447969ac700a84fb53d8b7504400744528e0bb23355e13a261f266ce4771fc8`  
		Last Modified: Thu, 21 Aug 2025 19:33:59 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce78aaf6cfc04da37a4110bfd74c30de2cf137f22e65525cfd26255afdc8232`  
		Last Modified: Thu, 21 Aug 2025 19:34:04 GMT  
		Size: 38.1 MB (38125419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644ecdb72685101a9e53ae7cd8fec7421371f5c4c28f84998d575a8db0ab36c1`  
		Last Modified: Thu, 21 Aug 2025 19:38:23 GMT  
		Size: 107.7 MB (107696671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc3a50c13cb1309665facc93ea3f97c96f6080a01679a244f8bea4b50cab8e0`  
		Last Modified: Thu, 21 Aug 2025 19:38:16 GMT  
		Size: 35.0 KB (34984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:29d61372f617169473dd874690b1eb8f48c6420b5cf78dc7c7179d9c14c6b2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5424045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0bdfec754b83aec337e57f29e1775a7969db21fbc38ba929524a99420c9f15`

```dockerfile
```

-	Layers:
	-	`sha256:07a22136eb8fe532f5f690f54a78497811c39bb09f0ca332cd1c8cad05c6dfb9`  
		Last Modified: Thu, 21 Aug 2025 20:17:57 GMT  
		Size: 5.4 MB (5400380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34956ce357291ad89fd94e3665be2b5c3a7e1664015b4c0d2d3f6392eff6143f`  
		Last Modified: Thu, 21 Aug 2025 20:17:57 GMT  
		Size: 23.7 KB (23665 bytes)  
		MIME: application/vnd.in-toto+json
