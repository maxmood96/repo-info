## `gradle:8-jdk17-ubi-minimal`

```console
$ docker pull gradle@sha256:9af742b3576c00d324f5dcda1c7bf8591950e75429fd6771321ddfa03fd67872
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

### `gradle:8-jdk17-ubi-minimal` - linux; amd64

```console
$ docker pull gradle@sha256:bd8e8bf474338f97e41fafc143021dea82f5178f3ba8188e38f9fa54f4ed3d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.9 MB (389921268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfbdc0bd69b5647bd4c8b08d633c56e30f8e578a2b328f460e362a0e5a83146`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:06:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:06:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:06:33 GMT
ENV container oci
# Wed, 15 Oct 2025 08:06:34 GMT
COPY dir:f15650dcc2939ee0c30865212b61e6718fd6c24de4e7967bf7b651b8f0b24352 in /      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:06:34 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:06:34 GMT
COPY file:16bf5aac480286f91e3031d4f1acb4e76fb8c3be38d180e4713a0efdc39d6bad in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:06:35 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:06:12Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Sat, 08 Nov 2025 17:58:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 08 Nov 2025 17:58:31 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:36 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:58:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:37 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:37 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:22:25 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:22:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:22:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:22:25 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:22:25 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:23:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 08 Nov 2025 18:23:16 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 08 Nov 2025 18:23:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 08 Nov 2025 18:23:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:23:18 GMT
USER gradle
# Sat, 08 Nov 2025 18:23:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:23:19 GMT
USER root
```

-	Layers:
	-	`sha256:2920d84eafa0cf94806ab58f0a2124f7b2d35bcbb06fc89a9106dcc28efe397a`  
		Last Modified: Wed, 15 Oct 2025 09:03:15 GMT  
		Size: 39.7 MB (39653524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1065367bed03b574d289037052f13ad45bce9ff9e2d6376ca30dbc6601929a1c`  
		Last Modified: Sat, 08 Nov 2025 17:59:04 GMT  
		Size: 16.6 MB (16603148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfb605769eec73700945a7b7dbf98bacd74f7c7aa525687cdc599fddff7a656`  
		Last Modified: Sat, 08 Nov 2025 18:22:21 GMT  
		Size: 144.9 MB (144852924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d800b8a7ad4976c00870e4f10b9a9d50f690f71dea02ae491022f1bcddd37f9a`  
		Last Modified: Sat, 08 Nov 2025 17:59:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24176df43dc3c8cc80123b86a853bc4347470a6b8ca742ae426ad74be6fc5490`  
		Last Modified: Sat, 08 Nov 2025 17:59:00 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56ec39f589a3e30aa88aa5f6a7ccc0f4fd5757ae402bb45e736fc734876649d`  
		Last Modified: Sat, 08 Nov 2025 18:23:07 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8eed46ba7e5b983bbace3ff91e10010287aeeee7cc1f0a2845dfed1c3a5cc76`  
		Last Modified: Sat, 08 Nov 2025 18:24:02 GMT  
		Size: 51.4 MB (51357699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fe1529f15f889edd94d3593675f433fe4a7262fc29908dba711fc951cac554`  
		Last Modified: Sat, 08 Nov 2025 18:23:39 GMT  
		Size: 137.4 MB (137395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e616165f0191e673ba812032f9c702232847d0868001360dc217977506acfb`  
		Last Modified: Sat, 08 Nov 2025 18:23:46 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:c0b2158330d133407c0ab6546ca1a82ed7d8aef94f0b0d652071aaa4ab11494f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e19a15ca938b9aa970d353d02f355cdfe39d9752408b62d6a28cf5331c02ff8`

```dockerfile
```

-	Layers:
	-	`sha256:687979ae10f7bd8850a894b6b7af8616f19dc77cc31b3c3f3be9494f109c51be`  
		Last Modified: Sat, 08 Nov 2025 21:27:16 GMT  
		Size: 5.4 MB (5390541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98773804dfbfe4dc515162ad7da9ea70630f8f175ca64b7d4ac2fa2ff9ba828`  
		Last Modified: Sat, 08 Nov 2025 21:27:17 GMT  
		Size: 23.6 KB (23599 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi-minimal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ead57b8d8bc6d2b65fc8092aeb70bc9d241e78e599720e082722033c5ff15576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.3 MB (386304870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe25fbf79253da94b1553e44ad11ebbaeb5fcbe5316fab294cad9b6f8c49ca8f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:10:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:10:52 GMT
ENV container oci
# Wed, 15 Oct 2025 08:10:53 GMT
COPY dir:a993e2e2ad3cf26c4ca4b583710869f381ee3e7df7d41715015a96348230e455 in /      
# Wed, 15 Oct 2025 08:10:53 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:10:53 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:10:54 GMT
COPY file:85de04d2096a64069474160b53ad5f2cfb18b7e3f3ec2a8d26b3946f32e004c9 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:10:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:10:36Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Sat, 08 Nov 2025 17:58:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:58:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:58:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:58:03 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 08 Nov 2025 17:58:03 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 17:58:10 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 17:58:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 17:58:11 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 17:58:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 17:58:11 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:23:08 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:23:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:23:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:23:08 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:23:08 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:24:04 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 08 Nov 2025 18:24:04 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 08 Nov 2025 18:24:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 08 Nov 2025 18:24:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:24:06 GMT
USER gradle
# Sat, 08 Nov 2025 18:24:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:24:07 GMT
USER root
```

-	Layers:
	-	`sha256:2602e1c5e8830fe80a6207359ce01e6c9b7d6848be663c4df1e03c724149b8a6`  
		Last Modified: Wed, 15 Oct 2025 09:30:32 GMT  
		Size: 37.9 MB (37896281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651dece7a6e73fb9ca899eabeb20e8f8f4bf839514ef4e06b6acb530e8f07ec2`  
		Last Modified: Sat, 08 Nov 2025 17:58:41 GMT  
		Size: 16.6 MB (16602800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41c5d1692fb061916b32cb81d79905385af6a001b2dc0ea6d88954d4a2d53f0`  
		Last Modified: Sat, 08 Nov 2025 18:23:05 GMT  
		Size: 143.7 MB (143685442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd434ef6c3645126fe28d24fafd9ade66aea57481ef9f334e572279b36d24cf8`  
		Last Modified: Sat, 08 Nov 2025 17:58:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6645bf2e242c2a98df077c7c3c2d6ce238615aaf9dc37a4ed1762a057c4bb7ae`  
		Last Modified: Sat, 08 Nov 2025 17:58:18 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79382b8fcdf2e864067d1814a13b516b35534ad30f73b6b03167c1aa92c1a0`  
		Last Modified: Sat, 08 Nov 2025 18:23:46 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985ab79cfde33f4b425789c62f0fda6c4c95ab9f9ad8b80414599c95271fd0c7`  
		Last Modified: Sat, 08 Nov 2025 18:24:37 GMT  
		Size: 50.7 MB (50661768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e61dce941fc6a34745407c27e4497d965a0d33d0aaf4fe7414e3d00a78a7c1`  
		Last Modified: Sat, 08 Nov 2025 18:24:27 GMT  
		Size: 137.4 MB (137395178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71478cc2d782cc75960d331fb9245b85091523b004703390dca0077b90847c0`  
		Last Modified: Sat, 08 Nov 2025 18:24:33 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:0996da2784483c07463726ac32e752c3b4a628b309ba091075cbedcd878972c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5413721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8adef9845bb85db15be3b4b41a8e1498aa071e4ff13247c1412f0116e29f36de`

```dockerfile
```

-	Layers:
	-	`sha256:7efcbaec8298ff60521baeb9d205a30a099321b2ba8136745466298768abfbd7`  
		Last Modified: Sat, 08 Nov 2025 21:27:21 GMT  
		Size: 5.4 MB (5389949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a749c58cfa756d91ae4f7e555abaf9062b9139609a470ef95ddbb1d2e7553213`  
		Last Modified: Sat, 08 Nov 2025 21:27:22 GMT  
		Size: 23.8 KB (23772 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi-minimal` - linux; ppc64le

```console
$ docker pull gradle@sha256:223f82206c2181d51191958ea764ae011096046bd2c8193cb9b1060a6300cf1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.5 MB (399503788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbbaf2de3e635c6bad827de6626317314151cac682654fc7e089e60b8e0a11d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:07:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:07:55 GMT
ENV container oci
# Wed, 15 Oct 2025 08:07:55 GMT
COPY dir:449eb2f239bac2d8d364a723cb091b20b453ccb6c9e9ef4542e774b1e6a3f931 in /      
# Wed, 15 Oct 2025 08:07:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:07:56 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:07:56 GMT
COPY file:a1ec773a4fe5bc79df5be7b721d463b5573cea3333f3a512f669f32fa8283a6b in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:07:56 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:07:44Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Sat, 08 Nov 2025 17:57:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:57:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:57:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:57:21 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 08 Nov 2025 17:57:21 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:14:35 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 18:14:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:14:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:14:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:14:38 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 20:14:33 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 20:14:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 20:14:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 20:14:33 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 20:14:33 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 20:24:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 08 Nov 2025 20:24:31 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 08 Nov 2025 20:24:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 08 Nov 2025 20:24:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 20:24:37 GMT
USER gradle
# Sat, 08 Nov 2025 20:24:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 20:24:39 GMT
USER root
```

-	Layers:
	-	`sha256:7d2fc558322651c1228b069dff5be5599bf4a7e595e3227e6de491f7067f1a45`  
		Last Modified: Wed, 15 Oct 2025 08:44:15 GMT  
		Size: 44.1 MB (44050495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd418b58a61783498a7a914a92baa56a29c3bdb5efae22fc9de5972b10f54d1d`  
		Last Modified: Sat, 08 Nov 2025 17:58:10 GMT  
		Size: 19.9 MB (19909128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c545b3c3323c1a259c7c89305aad21b17961a9ba28308e647c49005d5aa073bc`  
		Last Modified: Sat, 08 Nov 2025 18:15:21 GMT  
		Size: 144.5 MB (144547813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bd78a0f2b8d74e1576648189d42dd27271f7de84cfb0b0b40a7aceb809ac0c`  
		Last Modified: Sat, 08 Nov 2025 18:15:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8daf20e2a137d156696158a423617b3572ae419f18634a38c56967dffab4b3`  
		Last Modified: Sat, 08 Nov 2025 18:15:27 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223b3511d14ef4abb8a26a64f103561d9f4f3507e1946bfff240559ef9f3661a`  
		Last Modified: Sat, 08 Nov 2025 20:25:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234804be7d1c01da67b018351c79576226597989f6fc32611fed4c998188af62`  
		Last Modified: Sat, 08 Nov 2025 20:25:34 GMT  
		Size: 53.6 MB (53562271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734f482173f3bc65210721541140e352752174980d2b1199fe222e4e41907657`  
		Last Modified: Sat, 08 Nov 2025 20:25:25 GMT  
		Size: 137.4 MB (137395203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:befb35f8b65e96d194ffc1745cd94f7f675ed0287a7493b705400e5aa431e7e1`  
		Last Modified: Sat, 08 Nov 2025 20:25:30 GMT  
		Size: 35.0 KB (35010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:f240a8e88eb8e9eedb84f95c3c4bfb9acba481c1f500ce593cf72e921dff2c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5411527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ded7e5433d589fd306666915e5c4877fbecfdd358e16fbc45425cd0327aba4a`

```dockerfile
```

-	Layers:
	-	`sha256:3600913a38ee4d8c4abbd4bba98e9d55642a896c57e34d5f03142cb56e77d171`  
		Last Modified: Sat, 08 Nov 2025 21:27:27 GMT  
		Size: 5.4 MB (5387866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0f16e3568aea1c91d281c8c4fc146d1f6e6a5dbdf6981e9627628b09195ba49`  
		Last Modified: Sat, 08 Nov 2025 21:27:27 GMT  
		Size: 23.7 KB (23661 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi-minimal` - linux; s390x

```console
$ docker pull gradle@sha256:2a1d6876fbdc8d4f24768dcdb81544f61c21632dbd4ed685c0d30eda17052f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.2 MB (377170102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e1e9041e5294e3616452a6e4f85e41d8387ad4228cba67596715e43b8bc256`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Oct 2025 08:12:13 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 15 Oct 2025 08:12:13 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.6"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 15 Oct 2025 08:12:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 15 Oct 2025 08:12:14 GMT
ENV container oci
# Wed, 15 Oct 2025 08:12:14 GMT
COPY dir:c7531cf9ca81563f111865af7c21a35f1b40cdbceb45f292beb90b52a7f09fd7 in /      
# Wed, 15 Oct 2025 08:12:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 15 Oct 2025 08:12:14 GMT
CMD ["/bin/bash"]
# Wed, 15 Oct 2025 08:12:14 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 15 Oct 2025 08:12:14 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 15 Oct 2025 08:12:14 GMT
COPY file:c18f78822817f13e8af547877aa1bb6f7295fa27828e91bdb8605916bb9a08c8 in /root/buildinfo/labels.json      
# Wed, 15 Oct 2025 08:12:15 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "org.opencontainers.image.revision"="d1b15a34ce69ea214e1d32f1f501304f6b8b8c59" "build-date"="2025-10-15T08:12:03Z" "release"="1760515502"org.opencontainers.image.revision=d1b15a34ce69ea214e1d32f1f501304f6b8b8c59
# Sat, 08 Nov 2025 17:55:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 17:55:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 17:55:57 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 08 Nov 2025 17:55:57 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 08 Nov 2025 17:55:57 GMT
ENV JAVA_VERSION=jdk-17.0.17+10
# Sat, 08 Nov 2025 18:03:42 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='dc29ca6d35beb4419b4b00419b8a3dfbf5ae551e1ae2b046b516d9a579d04533';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.17_10.tar.gz';          ;;        ppc64le)          ESUM='2a29d1be61940c1bd639018c07f4622e1f145a7ef34e7294fee877e39226d9da';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.17_10.tar.gz';          ;;        s390x)          ESUM='76327b1d00c67f6be91717754fd85fc85ce496d48876f69accb9c53ed31dc546';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.17_10.tar.gz';          ;;        x86_64)          ESUM='992f96e7995075ac7636bb1a8de52b0c61d71ed3137fafc979ab96b4ab78dd75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.17%2B10/OpenJDK17U-jdk_x64_linux_hotspot_17.0.17_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Sat, 08 Nov 2025 18:03:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Sat, 08 Nov 2025 18:03:44 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 08 Nov 2025 18:03:44 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 08 Nov 2025 18:03:44 GMT
CMD ["jshell"]
# Sat, 08 Nov 2025 18:26:23 GMT
CMD ["gradle"]
# Sat, 08 Nov 2025 18:26:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 08 Nov 2025 18:26:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 08 Nov 2025 18:26:23 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 08 Nov 2025 18:26:23 GMT
WORKDIR /home/gradle
# Sat, 08 Nov 2025 18:32:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 08 Nov 2025 18:32:31 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 08 Nov 2025 18:32:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 08 Nov 2025 18:32:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 08 Nov 2025 18:32:43 GMT
USER gradle
# Sat, 08 Nov 2025 18:32:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 08 Nov 2025 18:32:44 GMT
USER root
```

-	Layers:
	-	`sha256:a42ec211faae823c9be27da6cd639f320fbf91a4d4f8d9a8428b8b1f4f661ad4`  
		Last Modified: Wed, 15 Oct 2025 12:11:19 GMT  
		Size: 37.8 MB (37759797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7057baef8e1e56074fbebcae2ebe9fc755e75d3f376cc35d8243e5172094c140`  
		Last Modified: Sat, 08 Nov 2025 17:56:51 GMT  
		Size: 16.5 MB (16457363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce5a53e0854b1ef9630b5a90ab7fd03241248d09d5466a1b1e32ec4aae2e7c8`  
		Last Modified: Sat, 08 Nov 2025 18:04:09 GMT  
		Size: 134.9 MB (134862205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fbc1509587b754005da402c0bb20b3c3bea36542b5756fd3a8b9b0b6b7df64`  
		Last Modified: Sat, 08 Nov 2025 18:04:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7823a461112cd247b0b2e38cef85d08de9f0ce23aa36e74908af0ca3249e0d1b`  
		Last Modified: Sat, 08 Nov 2025 18:04:19 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eb91557f201b08cafedf071daacf41c6878049e2e9c9b8f80ab1fb515cf6db`  
		Last Modified: Sat, 08 Nov 2025 18:34:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d14b50a124f153f6fb1f9639ac1ddd8b57857c21d80bf31e60b3f64993042e6`  
		Last Modified: Sat, 08 Nov 2025 18:34:08 GMT  
		Size: 50.7 MB (50656659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb803bee8af67b2a18d3939e7adf92c14e9186f0b7833921448518aab9c76376`  
		Last Modified: Sat, 08 Nov 2025 18:33:57 GMT  
		Size: 137.4 MB (137395202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6938cf0e6095af1f56a24fb3b239b5bd3c9d0e2fc01c65528202313c46582c9`  
		Last Modified: Sat, 08 Nov 2025 18:34:03 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi-minimal` - unknown; unknown

```console
$ docker pull gradle@sha256:2fdbdac2b775ebfa0057c5a50d84933d5be0bd5ecaf67904f9cde059357ce4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14edd0079fafc601ada81a11d462c0261ea400441ac2b82611268a85eeb2e8c`

```dockerfile
```

-	Layers:
	-	`sha256:5a9c799da8c1972d6e3bd1fbb8b03b5337c324f8b21f5ffc5e4955dbbad6bb4f`  
		Last Modified: Sat, 08 Nov 2025 21:27:32 GMT  
		Size: 5.4 MB (5377148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7775f64c1d56b844d5c898b080b1c58baa30cebde95c9b462823d4a9bf931282`  
		Last Modified: Sat, 08 Nov 2025 21:27:33 GMT  
		Size: 23.6 KB (23599 bytes)  
		MIME: application/vnd.in-toto+json
