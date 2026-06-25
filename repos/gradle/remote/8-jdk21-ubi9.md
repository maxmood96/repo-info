## `gradle:8-jdk21-ubi9`

```console
$ docker pull gradle@sha256:b4abfbb732e1839d457f4aafc1c90531eacede721219caef191b37cd98d4582a
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

### `gradle:8-jdk21-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:ffed79b33c766aa5a4f1abbabfdd3624e3721ae08d89ce514ccfb8386c4abfb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.5 MB (402548003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f8c23a9dc37af6dc3eee1b5b8f4b10d0f9a09070c40d1ff9cb83e2b01cfd82`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:11:46 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:11:46 GMT
ENV container oci
# Tue, 23 Jun 2026 05:11:46 GMT
COPY dir:f278a99c81d25e574e4095be97d2e212c8bd76544b73ffdab7eab4c5e42d12b6 in /      
# Tue, 23 Jun 2026 05:11:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:11:46 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
COPY dir:c2709a3d2c126f3448a9859c7e12a4347d4fe7ea0104c04c47ebdcbe0d9f7851 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:11:47 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:11:30Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:11:30Z" "architecture"="x86_64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:11:30Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:04:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:04:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:04:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:04:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:20 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 24 Jun 2026 23:04:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:04:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:04:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:04:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:04:28 GMT
CMD ["jshell"]
# Wed, 24 Jun 2026 23:17:35 GMT
CMD ["gradle"]
# Wed, 24 Jun 2026 23:17:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 24 Jun 2026 23:17:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 24 Jun 2026 23:17:35 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 24 Jun 2026 23:17:35 GMT
WORKDIR /home/gradle
# Wed, 24 Jun 2026 23:17:39 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 24 Jun 2026 23:17:39 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 24 Jun 2026 23:17:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 24 Jun 2026 23:18:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 24 Jun 2026 23:18:53 GMT
USER gradle
# Wed, 24 Jun 2026 23:18:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 24 Jun 2026 23:18:53 GMT
USER root
```

-	Layers:
	-	`sha256:689a2fa06433046ccdc79ee32d366190123758804fb645bc032123dc904e226b`  
		Last Modified: Tue, 23 Jun 2026 05:49:10 GMT  
		Size: 40.7 MB (40671135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e56292e6a3fee5d2c982366db7201d7e21e54edf5021b099e51e21b332c56b7`  
		Last Modified: Wed, 24 Jun 2026 23:04:45 GMT  
		Size: 27.7 MB (27660409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e384a0139f33e20f220df33fab37428578946f3b690ba5cea5a3ec5273e2490`  
		Last Modified: Wed, 24 Jun 2026 23:04:49 GMT  
		Size: 158.2 MB (158172693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282a1d559278d2bb6d4bc7be07d3c692d378ba524c64280dde7f6c9b8df4b522`  
		Last Modified: Wed, 24 Jun 2026 23:04:44 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0cd75f70f04c1f06b67703ba2ffe0fd853aba63c5910b1405f2bcf2aa9ce7`  
		Last Modified: Wed, 24 Jun 2026 23:04:44 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108c7b6ef8154b77ebd9c320b68be7f25ab2e034052f9e896d5fcd7a207b2dc6`  
		Last Modified: Wed, 24 Jun 2026 23:17:58 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d570eeb5d82928d2b61cd2ad45fd2484f6b46e8e01e696ec449a635d85087342`  
		Last Modified: Wed, 24 Jun 2026 23:18:01 GMT  
		Size: 37.9 MB (37916166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9251b114fc1ad5589deb0198bbf75cc391ae3d47ca346b427b787b2b7d09462`  
		Last Modified: Wed, 24 Jun 2026 23:19:11 GMT  
		Size: 138.1 MB (138068538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64451355e9d1306c7b0d4811772f45bfbde7e2a5f4c4fa0871f56465f52f5a20`  
		Last Modified: Wed, 24 Jun 2026 23:19:07 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:7755d936d609b33b5b0006644ffc3222b3f6c1929862234a03e1f9fda491c5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5432798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f430982e22d10c5964411370986e8cea6e5cff2e5ea7e4aed3d6279aafa2fb`

```dockerfile
```

-	Layers:
	-	`sha256:8b01bd3c9ada87ba051611bd956ccd4667163b8939662da95ae7ab9ce076eaf9`  
		Last Modified: Wed, 24 Jun 2026 23:19:07 GMT  
		Size: 5.4 MB (5408918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8267b10f302da08c03713f800f27656dd25e24158ce1657b3e1a7b836ca5b818`  
		Last Modified: Wed, 24 Jun 2026 23:19:07 GMT  
		Size: 23.9 KB (23880 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e98145d286550251f38b45efac19e509bfd91adf317b741b022750c99f792d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.1 MB (399085326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9ba57b29994ba380f1b4bad90db9de2634a781043ac5b917614e98f4c12b58`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:12:59 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:12:59 GMT
ENV container oci
# Tue, 23 Jun 2026 05:12:59 GMT
COPY dir:923fd04a317c8ab7292cc4c6490977e5f3d0a2e1ff9dc5a4ce7f5c95aef17062 in /      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
COPY dir:dffe6ac0f40d1fc4397ba26e90223bac1cf14e7dcba262c2807afbcac45f5ea3 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:00 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:36Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:36Z" "architecture"="aarch64" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:36Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:03:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:03:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:03:03 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:03:03 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:03:03 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 24 Jun 2026 23:03:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:03:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:03:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:03:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:03:33 GMT
CMD ["jshell"]
# Wed, 24 Jun 2026 23:14:25 GMT
CMD ["gradle"]
# Wed, 24 Jun 2026 23:14:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 24 Jun 2026 23:14:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 24 Jun 2026 23:14:25 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 24 Jun 2026 23:14:25 GMT
WORKDIR /home/gradle
# Wed, 24 Jun 2026 23:14:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 24 Jun 2026 23:14:31 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 24 Jun 2026 23:14:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 24 Jun 2026 23:15:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 24 Jun 2026 23:15:06 GMT
USER gradle
# Wed, 24 Jun 2026 23:15:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 24 Jun 2026 23:15:07 GMT
USER root
```

-	Layers:
	-	`sha256:989109f74f2ed8868dc53877eebf602a5b9e56448cce38c307c203e890a4c731`  
		Last Modified: Tue, 23 Jun 2026 06:05:10 GMT  
		Size: 38.8 MB (38805824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a2ec0a7edc88599608ffd0c7b8692b2d1aa437343dcc448a20400e53023b64`  
		Last Modified: Wed, 24 Jun 2026 23:03:17 GMT  
		Size: 14.1 MB (14059528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcd207c91f762f497d81718a4db67acd4de03c4beac8dcce7dc783ae50a650b`  
		Last Modified: Wed, 24 Jun 2026 23:03:53 GMT  
		Size: 156.5 MB (156464370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8af37a8495a18bd09ee5ca7d1a0cf1d62ccabb716b06fb1b45e9be0c5356ea`  
		Last Modified: Wed, 24 Jun 2026 23:03:50 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73ba5d9019f357de2b699b3085f227697b4c0300dcbb52a570ad2f0cc0edcee`  
		Last Modified: Wed, 24 Jun 2026 23:03:50 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da3a1bc6933bc1b6bf20f868fd3704990212ce16c1d38b4bea5cec2cb39216`  
		Last Modified: Wed, 24 Jun 2026 23:14:52 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b0076bdded754e544175091a29db10894b99ca2169fe07f47b75862a5cb1d3`  
		Last Modified: Wed, 24 Jun 2026 23:14:54 GMT  
		Size: 51.6 MB (51623664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a10d733a297b3dbd9a35c022647224a81f62c284197c031c7f3484330aa8758`  
		Last Modified: Wed, 24 Jun 2026 23:15:26 GMT  
		Size: 138.1 MB (138068542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a126501f115bcdcb59c48caa54d26dc278c2c90de68a3827c97912eb5e46a7a`  
		Last Modified: Wed, 24 Jun 2026 23:15:22 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:dbbbb8c7806e03a469273cb16f0810b9f00ab1893e97ba0a257e60f268aafbd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad2174f078718451f41c4af41daa24d97c7288996c30cc98815c94c5aecfa2a`

```dockerfile
```

-	Layers:
	-	`sha256:f4c1bdc7f75ba67d622f99e2e802809d6be728a1c9edab5f8656717ad874dc8a`  
		Last Modified: Wed, 24 Jun 2026 23:15:22 GMT  
		Size: 5.4 MB (5410722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8dc6539250fe914aee9eb1f2d92bde1744410caceff86f6fd10179812a8ba14`  
		Last Modified: Wed, 24 Jun 2026 23:15:22 GMT  
		Size: 24.1 KB (24053 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:f29ff46768b94701f5f2c3450558428e163e5d9ea42061000c5b2fcc8a84c1e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.4 MB (411382765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a9a46c93c23504e0561a6000fd25ec2b083627140a54771524914cd4071e07`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:13:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:13:01 GMT
ENV container oci
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:4d2a3ebfba3e6886b6504d8dd92beaac194e548e40aa4bca182adbaa9be02afc in /      
# Tue, 23 Jun 2026 05:13:02 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:13:02 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:b7827d131ad066b0f131c7ebfb16ff261b70c3cbb8cf357ab0913f8aa1eef055 in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:13:02 GMT
COPY dir:b7827d131ad066b0f131c7ebfb16ff261b70c3cbb8cf357ab0913f8aa1eef055 in /root/buildinfo/      
# Tue, 23 Jun 2026 05:13:02 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:12:46Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:12:46Z" "architecture"="ppc64le" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:12:46Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:01:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:01:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:01:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:01:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:01:50 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 24 Jun 2026 23:07:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:07:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:07:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:07:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:07:49 GMT
CMD ["jshell"]
# Thu, 25 Jun 2026 02:46:40 GMT
CMD ["gradle"]
# Thu, 25 Jun 2026 02:46:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 25 Jun 2026 02:46:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 25 Jun 2026 02:46:40 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 25 Jun 2026 02:46:40 GMT
WORKDIR /home/gradle
# Thu, 25 Jun 2026 02:47:00 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Thu, 25 Jun 2026 02:47:00 GMT
ENV GRADLE_VERSION=8.14.5
# Thu, 25 Jun 2026 02:47:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Thu, 25 Jun 2026 02:49:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 25 Jun 2026 02:49:36 GMT
USER gradle
# Thu, 25 Jun 2026 02:49:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 25 Jun 2026 02:49:38 GMT
USER root
```

-	Layers:
	-	`sha256:4bac72a9a1f43367def803d06c2dab63b4bb0e322cb08ee3db80259d84e62045`  
		Last Modified: Tue, 23 Jun 2026 06:12:06 GMT  
		Size: 45.1 MB (45144751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f99e1bd1d0e0245b9ff9de06dc4f155f0170e63761b11e9c13863eabbea391`  
		Last Modified: Wed, 24 Jun 2026 23:02:32 GMT  
		Size: 15.2 MB (15157790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b8479e3d31c2805ff9f4e94d7435b44f176c767ea97fd77e7b6d356e17176f`  
		Last Modified: Wed, 24 Jun 2026 23:08:27 GMT  
		Size: 158.3 MB (158348475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb1f77a4fa77afd48d893518750cdfe352c12cff949d37a6d94dd4f75cda1ff`  
		Last Modified: Wed, 24 Jun 2026 23:08:23 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b8f4acfaabc8ef24e93d311171fa72ff7f2e9099940a72a95e33a4c739ea2e`  
		Last Modified: Wed, 24 Jun 2026 23:08:23 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabaa0646c0a98e7f1775ba1ab22c38c381ac7170e3ee14cde4fea713761675d`  
		Last Modified: Thu, 25 Jun 2026 02:47:47 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb4cab9f00b71405a9aed3aeaf3f00975ead64307cb62c49e75828ecda06d8c`  
		Last Modified: Thu, 25 Jun 2026 02:47:50 GMT  
		Size: 54.6 MB (54624312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff76904d95449aa33b8df326831022b02e691afc16f0db06f35e478dd2545b3`  
		Last Modified: Thu, 25 Jun 2026 02:50:23 GMT  
		Size: 138.1 MB (138068544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5012d63e51623dcb952571ba3caa969754bed1b664e51b319bb935aa45737e`  
		Last Modified: Thu, 25 Jun 2026 02:50:19 GMT  
		Size: 35.0 KB (35014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:089482e537bd2d3c01705d0636545e239bc84667f2493ef5b9d74b13ac2b88ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5432618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebd4b1ad2956aa5a29162750c4d4294a3ecc8bb1d5d10095aab42abedbcdd95`

```dockerfile
```

-	Layers:
	-	`sha256:40423dc4ef731c35b042e531015850bd1c77cf841f5e8d2855eee163a963a7bd`  
		Last Modified: Thu, 25 Jun 2026 02:50:19 GMT  
		Size: 5.4 MB (5408677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2be1ed0459860bdce872ae17f87f5e7f0595dabb16e0786bf34e567bcf852d50`  
		Last Modified: Thu, 25 Jun 2026 02:50:19 GMT  
		Size: 23.9 KB (23941 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:9b95b5371f6e206e9ec1c374cb9570cef423d0b32619b2b980ccc5385a3576ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.9 MB (389867271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d862da17808d13608f1bfda7bff940ba5401d605153c45915b4c92b75595105`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.openshift.expose-services=""
# Tue, 23 Jun 2026 05:18:00 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 23 Jun 2026 05:18:00 GMT
ENV container oci
# Tue, 23 Jun 2026 05:18:00 GMT
COPY dir:27877c357368aea512a88a6f3ff986d2f2cae38facf5c958fc65210886393092 in /      
# Tue, 23 Jun 2026 05:18:00 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 23 Jun 2026 05:18:00 GMT
CMD ["/bin/bash"]
# Tue, 23 Jun 2026 05:18:00 GMT
COPY dir:93599b4d15b0e179c067caa1878c815ffdcb1bde2382dffed0b86ba833b3047a in /usr/share/buildinfo/      
# Tue, 23 Jun 2026 05:18:00 GMT
COPY dir:93599b4d15b0e179c067caa1878c815ffdcb1bde2382dffed0b86ba833b3047a in /root/buildinfo/      
# Tue, 23 Jun 2026 05:18:01 GMT
LABEL "org.opencontainers.image.created"="2026-06-23T05:17:03Z" "org.opencontainers.image.revision"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "build-date"="2026-06-23T05:17:03Z" "architecture"="s390x" "vcs-ref"="e834ed7be4fa69fe8faf5574157c5c65992ace09" "vcs-type"="git" "release"="1782191395"org.opencontainers.image.created=2026-06-23T05:17:03Z,org.opencontainers.image.revision=e834ed7be4fa69fe8faf5574157c5c65992ace09
# Wed, 24 Jun 2026 23:01:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:01:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:01:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:01:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:01:53 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 24 Jun 2026 23:03:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:03:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:03:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:03:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:03:28 GMT
CMD ["jshell"]
# Wed, 24 Jun 2026 23:07:38 GMT
CMD ["gradle"]
# Wed, 24 Jun 2026 23:07:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 24 Jun 2026 23:07:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 24 Jun 2026 23:07:38 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 24 Jun 2026 23:07:38 GMT
WORKDIR /home/gradle
# Wed, 24 Jun 2026 23:07:50 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 24 Jun 2026 23:07:50 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 24 Jun 2026 23:07:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 24 Jun 2026 23:08:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 24 Jun 2026 23:08:57 GMT
USER gradle
# Wed, 24 Jun 2026 23:08:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 24 Jun 2026 23:08:57 GMT
USER root
```

-	Layers:
	-	`sha256:027b6558e15fa03e681ac683754dd2058185e2be499788f5e5a422bfa61b34db`  
		Last Modified: Tue, 23 Jun 2026 06:11:50 GMT  
		Size: 38.8 MB (38754261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ba193d3988998f0967fb407a4f53a44e2a2ac7df01730ea0a45fcebd52490`  
		Last Modified: Wed, 24 Jun 2026 23:02:22 GMT  
		Size: 13.9 MB (13892087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33277d916e15c2e13c2e07e11021d5991e58e1dcec00b9b7f5b5a0079f19e128`  
		Last Modified: Wed, 24 Jun 2026 23:03:54 GMT  
		Size: 147.4 MB (147390156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6067b3d020a4ba91921bfbd4aa5ea4b3c8b40bcfe7b8ec0f63bad8a3fdf26116`  
		Last Modified: Wed, 24 Jun 2026 23:03:46 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e239dc979e0cd09a2253b6ea23b0bcd92c2260eea77fd2c3ddba33ab5c49510b`  
		Last Modified: Wed, 24 Jun 2026 23:03:51 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee38de117077461831a6f42560ac6c82925d9a04cc8878ea9ed84b50b8aa0650`  
		Last Modified: Wed, 24 Jun 2026 23:08:25 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2b2d079b4cc545335f079aa540d10a126430019694782921af270cb75ed4b8`  
		Last Modified: Wed, 24 Jun 2026 23:08:28 GMT  
		Size: 51.7 MB (51723358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576e0e5908173da2772a7c6d7da93e99654e183eafa1a6f024e9b9ce4f9125b7`  
		Last Modified: Wed, 24 Jun 2026 23:09:25 GMT  
		Size: 138.1 MB (138068537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c8fe67bec7c192eb6c0272eb3f7ef54237156bb6eea7bb3e811b2aaa89bae2`  
		Last Modified: Wed, 24 Jun 2026 23:09:22 GMT  
		Size: 35.0 KB (35003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:86771ae0f8c22b7e929e77ec6b1b7356eb1bd4157b1afc151c1382535663dbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5421801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba349ec5f9291d66aa54a9a99e40d348582fe9b5e2e894ae4f1bb79638148c3`

```dockerfile
```

-	Layers:
	-	`sha256:59af9d6883c6d874814f8ee6fd349c6544bc2dc55fc5777a46e1f411462ebdb3`  
		Last Modified: Wed, 24 Jun 2026 23:09:22 GMT  
		Size: 5.4 MB (5397921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b9ddcfc0af90fa7aadce58b8e1a75aaf65fe518250771eb7442c975df7e73f`  
		Last Modified: Wed, 24 Jun 2026 23:09:22 GMT  
		Size: 23.9 KB (23880 bytes)  
		MIME: application/vnd.in-toto+json
