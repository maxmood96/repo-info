## `gradle:ubi`

```console
$ docker pull gradle@sha256:b8bba7a8a722ac0f40b826bb99f1e5ecfac7eef2ca732039ac26dc7b95381bd0
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

### `gradle:ubi` - linux; amd64

```console
$ docker pull gradle@sha256:7c5b5ee4a8ad06896f3d49a537099bc86340902a4fc86ee8f22168431cbdd434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 MB (396335521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd932133777428a1c54dbebda968b517b31fb9881a81c0788a0a9ac6b40c1fde`
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
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeccba03a7a3ec018a4db636c2a0d62a54d357430f7b06bf72af67b3bc4f6ea`  
		Last Modified: Wed, 13 Aug 2025 23:02:52 GMT  
		Size: 27.5 MB (27538846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6210a3ddff8eb74bb18263db2faa23b02bb81ab5f402d8ca69d386f5732aba`  
		Last Modified: Wed, 13 Aug 2025 23:11:06 GMT  
		Size: 157.8 MB (157807529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359dc5f5daba618664857c15e5867a7916767a66a5b9b06f8759934b0cb6d20d`  
		Last Modified: Wed, 13 Aug 2025 23:02:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbb0c3b4f0700a403303e981019b4c1a3219b48a219894e9e3f6b1bce9af728`  
		Last Modified: Wed, 13 Aug 2025 23:02:18 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cca0651079f9c1c7880a172f2f781a858bc162a45649446ff712604f7ebe6d`  
		Last Modified: Wed, 13 Aug 2025 23:11:46 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6bbe476654d13b6986cd38a8f857377682e1f2b6c51d97cdb562d19b5ddc25`  
		Last Modified: Wed, 13 Aug 2025 23:11:52 GMT  
		Size: 36.8 MB (36797957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8469d147fbcf1b78453de382fcfe1458a02dde883df451863d11e5eb6284517`  
		Last Modified: Thu, 14 Aug 2025 03:28:36 GMT  
		Size: 134.5 MB (134480836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f967d5b0e65cfa9d9449182d0fe8f32e913e9b4944a1989238199812a450a14`  
		Last Modified: Wed, 13 Aug 2025 23:11:47 GMT  
		Size: 54.9 KB (54892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:06c708dc04099f35ae3a22bb57ba45e6226ad271d60c4576d2b0fca273288980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c9357ef55dbb5ce8f82137974b58a8da2ffd24e504db483a03ca6e3daa6dc2`

```dockerfile
```

-	Layers:
	-	`sha256:be9bb047f97b5b6da41715f7ac55145b128d5f965abdc7aaabd822c2c46bafb0`  
		Last Modified: Thu, 14 Aug 2025 02:25:20 GMT  
		Size: 5.4 MB (5378642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84f3f93fad7f3818e2260c2003b8eaa85ccf50607d9bb17c44fe1f1f4306a8d6`  
		Last Modified: Thu, 14 Aug 2025 02:25:21 GMT  
		Size: 24.9 KB (24864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cd0165bbe5f5a6a8457048fc45566a25a78cf65f599b59499c104d2721e74d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.7 MB (392680156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada94280cdf5b2f2f63796ea2dde3b070b6c4cacb3413e1073979155d336b951`
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
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:ae68ff313f78851fbf66137c0a49a327986447045fa7f2497adbc1b57f88db56`  
		Last Modified: Thu, 07 Aug 2025 18:09:51 GMT  
		Size: 37.8 MB (37819116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52d35c18e9a72456397f9eeedbd19f9dc8600f65f4d8fd5d96621d533551288`  
		Last Modified: Thu, 14 Aug 2025 09:09:50 GMT  
		Size: 28.0 MB (27982673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4435068303bcc72148bcc61ca7d6f59073debddb9607802bb74e83d104e9606`  
		Last Modified: Thu, 14 Aug 2025 13:14:24 GMT  
		Size: 156.1 MB (156084803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be1e9df695da84f4aa34b19702784d6bae17ed4a3545035cc6928257175edb`  
		Last Modified: Thu, 14 Aug 2025 09:16:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8c952f099211acf6c85f8eb50a1d52a744f1addfda53e6ae7e986a9bc8c1b0`  
		Last Modified: Thu, 14 Aug 2025 09:16:35 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfe1b66db5ac38d377de72f2e9cf06f2b416ef78e3963f4d9cd720f08720a5b`  
		Last Modified: Thu, 14 Aug 2025 11:42:23 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088b28753c5ff3606876e3c6b61b16b3170a6dc25e027a259380e8da07fdd7ff`  
		Last Modified: Thu, 14 Aug 2025 14:31:17 GMT  
		Size: 36.2 MB (36249044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd00b4ef1e4949ab056d871567c0ee9061ad4091e5343690088e87b10302e0e`  
		Last Modified: Thu, 14 Aug 2025 17:15:57 GMT  
		Size: 134.5 MB (134480832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffcab5da111ab8bc75e5d5bbcf49ed97ab59b5bd337b3650e5082af4db0f1a6`  
		Last Modified: Thu, 14 Aug 2025 11:42:24 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1dbd57687665a2819dc51ced47e51d78aa397f77795b5e0360605aa9690551d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5403183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9563a334092e58919aff5caed0474b8921f4d5f1659fe334806aa5dff3e20ae`

```dockerfile
```

-	Layers:
	-	`sha256:5eeb9aad880e2b11f69749878e0f0d1275fa241500b7c60b6e8827a00fe94a7c`  
		Last Modified: Thu, 14 Aug 2025 14:25:24 GMT  
		Size: 5.4 MB (5378098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e0af5b8c7923e9fa71112c34928a7c5c1c70c32eb9a33126aec16766b98df0`  
		Last Modified: Thu, 14 Aug 2025 14:25:25 GMT  
		Size: 25.1 KB (25085 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:1b78bb7c7cc3b8f9adb55c06b95def67b10b15aeb0ec2a43ad717d2fddab52e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.6 MB (404643198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05eaa57be40e9dba732deb2925709edeb2b4f4e1dcb9f7ca9946074a160e87c`
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
COPY dir:b1e34ea7a28362356126333145a3caa4ced0141e04688d16b04ab649c669f43c in / 
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Jul 2025 17:27:11 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Thu, 31 Jul 2025 17:27:11 GMT
LABEL "build-date"="2025-08-07T16:44:50" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Jul 2025 17:27:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 17:27:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:aba3f1acf76208b8b62efdeedca86eb113101be1a85516cf6b0aae00d20e9d93`  
		Last Modified: Thu, 07 Aug 2025 18:09:54 GMT  
		Size: 44.1 MB (44060283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b238a99b2c6469409aa73a74b213065b6dcf7ea4be7280b0870ff8e470e4ff5e`  
		Last Modified: Thu, 14 Aug 2025 04:46:37 GMT  
		Size: 30.0 MB (29975842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d029fa95d5a8c56e93bdaff7d123b61dd4bc3ac94d9690f287fffd90d47ba6d`  
		Last Modified: Thu, 14 Aug 2025 07:16:27 GMT  
		Size: 158.0 MB (157965639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c4388e5f7488ca44aa2d6fbd56d4370b21e8ab850b33b77f8506cf5d678b36`  
		Last Modified: Thu, 14 Aug 2025 04:59:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66166b2a78c8613074ba3c8d071e860713509949df5148b1c94859f16beb034`  
		Last Modified: Thu, 14 Aug 2025 04:59:02 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90fe5e5f7b4bf4b6852e17daa0a0b084b7c8ccd565f91eae5de15c28e3b2373e`  
		Last Modified: Thu, 14 Aug 2025 12:06:30 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26414ae651f198bb72b2537b277efb27204f74fdde73dfe696d968174cc4bcd1`  
		Last Modified: Thu, 14 Aug 2025 12:06:35 GMT  
		Size: 38.1 MB (38121435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28cb90411f1021cb60c700327bc1ded79ceeb1dcdb41c61816d917f3ff2215b`  
		Last Modified: Thu, 14 Aug 2025 12:14:22 GMT  
		Size: 134.5 MB (134480835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3085fba6c5d0449bbac10d34171d1dc9fdb8ff787f9b623de654b7440c5860e9`  
		Last Modified: Thu, 14 Aug 2025 12:06:30 GMT  
		Size: 35.0 KB (35004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:841598c9df961eb321f2eb9778113f85511576ae7375fea9e9fece5cdc893785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb894210c06e0e1087aa1f014ee25a94c268e50f1cd18a281d490f76c3cd97a`

```dockerfile
```

-	Layers:
	-	`sha256:62906565532320ff325c18affbbf67fc6bb70f078cfc5dcbe28833264b8b2dd6`  
		Last Modified: Thu, 14 Aug 2025 14:25:30 GMT  
		Size: 5.4 MB (5375991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10508eb6b866912495ecd8d2d5db5bc2b09c3bc886502242fa6542f96ee6fc5b`  
		Last Modified: Thu, 14 Aug 2025 14:25:31 GMT  
		Size: 24.9 KB (24950 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:ubi` - linux; s390x

```console
$ docker pull gradle@sha256:2f0d79ec9cfaf44000e96d0971b3e9f509c475de1f7ee20c459df452128b4920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383293878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b2facf34a5a4090082d6a7349222cfc08d33bc2e39d0aa39c7daa93973b061`
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
ENV JAVA_VERSION=jdk-21.0.8+9
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e5c41a1ab0865ea5de9b4529bf8526005f1d4593090845387d14fe450ce39c33';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64le)          ESUM='a24e869b8e563fd7b9f7776f6686ca5d737c8d1c3c33c9b72836935709b44a34';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='a84e3cbf8bb5f8a313e06b790c7bc388687ba00262e981f5e33432ebd4d34356';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        x86_64)          ESUM='f2dc5418092c43003db8f9005c4a286e1c0104fea96ccdd49e8ebd037cac9219';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
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
	-	`sha256:3863354635407eda9f82b3b7359cf6843bddcc6f39480eb7539bc52c29dfeb65`  
		Last Modified: Thu, 14 Aug 2025 07:16:13 GMT  
		Size: 147.0 MB (147026238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba5b312c27f929a6714731dba93106fe5c2abe0bb1453032541e137ffb9cc51`  
		Last Modified: Thu, 14 Aug 2025 04:06:30 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef8be03127f7068d8164ebd8fddb121fab0019ddad29da73bdaf2aeca32360`  
		Last Modified: Thu, 14 Aug 2025 04:06:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afaf9dfc03a409b12c392f80e984dc103c8712c631b3e8392eb9977e6f7b09e3`  
		Last Modified: Thu, 14 Aug 2025 10:47:43 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d51bc29d2b42fba34c3faf26ef4c17edf1126b4ff597710bed00ce8bd5681d`  
		Last Modified: Thu, 14 Aug 2025 10:47:55 GMT  
		Size: 36.4 MB (36429305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7e76c892243bad841a871037b1c694d5a0a8cfea1b2f25d9041d8824ecc776`  
		Last Modified: Thu, 14 Aug 2025 11:12:42 GMT  
		Size: 134.5 MB (134480837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3df1a453ba75b2a02a5005468099809aae75b07a09d27d1cde7d43464c43b6`  
		Last Modified: Thu, 14 Aug 2025 10:47:44 GMT  
		Size: 35.0 KB (35012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:f7dd8cffb2e21fb46b425653c8b6b715ab724c846de57a486f3b87433a8de9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5390113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea8eea78fe05c4ab5ea1c41311a5e17ab15a39c509da256a637174db7bcb7b0c`

```dockerfile
```

-	Layers:
	-	`sha256:0577a7c6311f2443d479a9483e02163c6600bf455b6fc5602fb740d2efbd502a`  
		Last Modified: Thu, 14 Aug 2025 11:23:34 GMT  
		Size: 5.4 MB (5365249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b3fd9d6abb54e17800590b9f44fd8f90ef43420ddea259d47463ca23ce4d1f`  
		Last Modified: Thu, 14 Aug 2025 11:23:34 GMT  
		Size: 24.9 KB (24864 bytes)  
		MIME: application/vnd.in-toto+json
