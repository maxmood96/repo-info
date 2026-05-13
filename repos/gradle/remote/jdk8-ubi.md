## `gradle:jdk8-ubi`

```console
$ docker pull gradle@sha256:da129f22f88a8e558d8eeaba6c00a734d27b5366bad0130aa695ee538be329f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:jdk8-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:d4e2d4de03a1286fb3c9c0dbceb7ba4290ff957a2e2f95451c7b50d07d5c5f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300413936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ced62ef7921e0ef42b290ac37b575f93af2864190a4751fa9cbb018dbe3132`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 05:07:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:07:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:07:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:07:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:07:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:07:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:07:30 GMT
ENV container oci
# Tue, 12 May 2026 05:07:31 GMT
COPY dir:5370c41d6d8459b92eabd7b14d9158353a8d692cfb39a86c0ad6f0e8377d5a95 in /      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:07:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
COPY file:14972e13093e3eed917450ec88ead3bcd5bf561d5ae0ced6252f2569fa2669a1 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:07:31 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:07:12Z" "org.opencontainers.image.created"="2026-05-12T05:07:12Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:07:12Z
# Tue, 12 May 2026 23:33:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:08 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:08 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 23:33:12 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 23:33:13 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 May 2026 00:13:48 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:13:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:13:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:13:48 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:13:48 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:51 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:51 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 13 May 2026 00:13:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 13 May 2026 00:13:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:54 GMT
USER gradle
# Wed, 13 May 2026 00:13:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:13:54 GMT
USER root
```

-	Layers:
	-	`sha256:c06b8ad3393fea673394e067fccddfc7ef6d8cee753eba4c4dcd5d67792bfd4b`  
		Last Modified: Tue, 12 May 2026 06:00:36 GMT  
		Size: 40.0 MB (40022633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1696ea29688df8011506b4999bbe15b213a04f92833774374ecdeae209b755dd`  
		Last Modified: Tue, 12 May 2026 23:33:28 GMT  
		Size: 30.4 MB (30368186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0896fb85cfc1736c4dcb4217c87647b3a1fbc9d2b115ea6417f6226d9be7ca6`  
		Last Modified: Tue, 12 May 2026 23:33:29 GMT  
		Size: 55.2 MB (55199121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c45f537f9f185ce42263d683f8657aece553c0cb080b3dcaf001733997f488`  
		Last Modified: Tue, 12 May 2026 23:33:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e55825d37138248dc12da2257ed01a242b08ad2c27842457c4c9b6379aaa63`  
		Last Modified: Tue, 12 May 2026 23:33:27 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44f594b4d0035fdb5ee06b9c4bb0af3bdfe73e0cd2f59cc8ad79628f3b8a4ba`  
		Last Modified: Wed, 13 May 2026 00:14:10 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feaa1e3c04e86b25a45f2a22e213cb4ba36c1f334fff3e229f8e5736be6695b`  
		Last Modified: Wed, 13 May 2026 00:14:11 GMT  
		Size: 36.7 MB (36696198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76185c9e67682a061b7524a60a182199d6f374cb6f0faa921a1d704a8842e9b7`  
		Last Modified: Wed, 13 May 2026 00:14:14 GMT  
		Size: 138.1 MB (138068537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb45cb1929070991df1de439104c4ec44d8c45eefb1890e99521b3b411d8d39`  
		Last Modified: Wed, 13 May 2026 00:14:10 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1eb6869ad2380d76662a812a7f06e1e2b8e53078919dec30f603823f14a28e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5549927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef3e2b9287bf90341b25919751dce7745cf2b90858dd8c3927de416a36b8868`

```dockerfile
```

-	Layers:
	-	`sha256:07087a71b2ff7b6ae7a2722c0c73a99429e8c08534a034bb2d870b72870119e9`  
		Last Modified: Wed, 13 May 2026 00:14:10 GMT  
		Size: 5.5 MB (5525510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fd4b1173ac62e683ffe577d5a19fd37804054a4ecca33532e1c66a38589ed48`  
		Last Modified: Wed, 13 May 2026 00:14:10 GMT  
		Size: 24.4 KB (24417 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:133ff119ba77530e23abb8ff35d6ec1bdf6902b08223bc6f25a7d1640ac490e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297424395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1da8a62acd3af1924b29b5e837c0d986cbf6df86472bb64efd4eb60425d47f1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 05:08:30 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:08:30 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:08:30 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:08:30 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:08:30 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:08:30 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:08:30 GMT
ENV container oci
# Tue, 12 May 2026 05:08:31 GMT
COPY dir:1ccd99245be3a0b58a1846f076e5b2ceb5e84e683dd2697432c08ac554789d9d in /      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:08:31 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
COPY file:cf956423e241a9e8b50b424962675080490b78c30504a00193ac8d9c11b9a880 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:31 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:08:17Z" "org.opencontainers.image.created"="2026-05-12T05:08:17Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:08:17Z
# Tue, 12 May 2026 23:32:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:32:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:32:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:32:49 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:32:49 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 23:32:54 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 23:32:54 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:32:54 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:32:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 May 2026 00:13:50 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:13:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:13:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:13:50 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:13:50 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:54 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:54 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 13 May 2026 00:13:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 13 May 2026 00:13:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:56 GMT
USER gradle
# Wed, 13 May 2026 00:13:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:13:57 GMT
USER root
```

-	Layers:
	-	`sha256:cd21d11a73b4a3fb6683533da05d561785e6bdfe61eb163870493206db32b8fc`  
		Last Modified: Tue, 12 May 2026 06:10:38 GMT  
		Size: 38.2 MB (38205025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f897ea2931727f712951b47e3f004b094bb5e3a2db3fc897741c160227cdadbd`  
		Last Modified: Tue, 12 May 2026 23:33:08 GMT  
		Size: 30.8 MB (30789041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5943d0ed177ac286c1a5edb6c53a06a6a3e9530e86d277664f089ab34df3935f`  
		Last Modified: Tue, 12 May 2026 23:33:09 GMT  
		Size: 54.3 MB (54273437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddae99603a6ac8d4b6d7398d7e216741e0334648f8ae3294b7117ae0c215d472`  
		Last Modified: Tue, 12 May 2026 23:33:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c64530f639bcac5388c90345fd764af8e28034a0cb0f4da756cf8b3c3cc908`  
		Last Modified: Tue, 12 May 2026 23:33:08 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ef19c7f1703510b319496c16817356a93798e049f12b2dd7cb97cd42070794`  
		Last Modified: Wed, 13 May 2026 00:14:12 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d2af626ccb7c86e017bbda731d7c35473ec961fc117ba555bbff1fe75c0ec6`  
		Last Modified: Wed, 13 May 2026 00:14:14 GMT  
		Size: 36.0 MB (36024449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922049f4488b4b6861c45a9402225037849648aae2049a8c47dc1b3663d72365`  
		Last Modified: Wed, 13 May 2026 00:14:16 GMT  
		Size: 138.1 MB (138068549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b623156402e91456ca36f39691f07bd413fb7959d26f4ae78550c51e77f121e`  
		Last Modified: Wed, 13 May 2026 00:14:12 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:dd481a542872014398b956d60689300894fed7b80063e41d402f6ecc3761c2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5550252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347b28c58e2d5dc4e490d30086538fc7571b0cf763691974ccbeeb1c1ffd13f8`

```dockerfile
```

-	Layers:
	-	`sha256:2992addc0e4690945e7bc4890e4553f616e26abc56bb71d9fbb34c75d3483fd2`  
		Last Modified: Wed, 13 May 2026 00:14:13 GMT  
		Size: 5.5 MB (5525640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:134822efabff9f6535af0e2e0e20bb37f3f4b85d859fe3d88c4e1b5a19027077`  
		Last Modified: Wed, 13 May 2026 00:14:12 GMT  
		Size: 24.6 KB (24612 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:fc5ec8d7d2e3a3c9b60dbea7f16ca3cc2e6b27a50e92c9c20eea4a3cd1d678ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305988070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87803cf3042aa5264af99cdce8a46b844c0f0f06651fff3fd7e765ffc7d88cee`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 05:08:36 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:08:36 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:08:36 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:08:36 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:08:36 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:08:36 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:08:36 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:36 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:08:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:08:37 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:08:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:08:37 GMT
ENV container oci
# Tue, 12 May 2026 05:08:37 GMT
COPY dir:a355654efba77c17476e6a7d5b5c7ad113dd460739ab9901deec15db41210d83 in /      
# Tue, 12 May 2026 05:08:37 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:08:37 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:08:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:08:37 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:08:38 GMT
COPY file:b6d86ec52d4ff251e9a69e4177680b9b3b6e71d2c630134454bededfdfd3098c in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:38 GMT
COPY file:b6d86ec52d4ff251e9a69e4177680b9b3b6e71d2c630134454bededfdfd3098c in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:08:38 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:08:26Z" "org.opencontainers.image.created"="2026-05-12T05:08:26Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:08:26Z
# Tue, 12 May 2026 23:31:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:31:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:31:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:31:48 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:31:48 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 23:31:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c2253b986909c20f79d6de7a0cb957f89c243df57615897836046e24d2e5257';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_aarch64_linux_hotspot_8u492b09.tar.gz';          ;;        ppc64le)          ESUM='867e477e0a54159c7b774c55cfb046767120b1de43f705fa775ece74ea39e341';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u492b09.tar.gz';          ;;        x86_64)          ESUM='da257f161d7f8c6ca5b0e5d9e4090f65ac28c5e398072e68b8ae87988b1d1a2e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u492-b09/OpenJDK8U-jdk_x64_linux_hotspot_8u492b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Tue, 12 May 2026 23:31:58 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:31:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:31:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 13 May 2026 00:16:28 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:16:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:16:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:16:28 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:16:28 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:16:39 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:16:39 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 13 May 2026 00:16:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 13 May 2026 00:16:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:16:43 GMT
USER gradle
# Wed, 13 May 2026 00:16:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:16:46 GMT
USER root
```

-	Layers:
	-	`sha256:79d0e019ce895d0aca184904f5a8e1c238e93edc928ef6e5b2e268c9ea088d61`  
		Last Modified: Tue, 12 May 2026 06:11:10 GMT  
		Size: 44.4 MB (44437382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbdf1fc5ff833d1acc4507cdc17a2bf17961989ce6e84f818cc2b5117051d29`  
		Last Modified: Tue, 12 May 2026 23:32:28 GMT  
		Size: 32.8 MB (32841724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2bb01d98ac75631cdd6268c95f459415141f13ba2fb2301fdd8c7ef5050c0f`  
		Last Modified: Tue, 12 May 2026 23:32:28 GMT  
		Size: 52.7 MB (52669677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3799e7e6c9ad83ab8dc35f49d41e66132b7797f14c84eee7e5c3b83f338ea1b9`  
		Last Modified: Tue, 12 May 2026 23:32:25 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c208ce8569d9779393f8cdc14f1c1c1042bcc8e5657302f46cac55e88a42b18`  
		Last Modified: Tue, 12 May 2026 23:32:27 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa37befa8a0c512a4205eca2ec5625a3585f91f79934af21173be8f37a20195`  
		Last Modified: Wed, 13 May 2026 00:17:18 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826a4abdca4d3166d96fe0c8ef43f3002b3bb179a1765d7b91d86d61f9c05a7c`  
		Last Modified: Wed, 13 May 2026 00:17:20 GMT  
		Size: 37.9 MB (37931378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49537bfcdbd35effd375244b354185b757ad85bf733ff26f9eee2ed4bf90d14`  
		Last Modified: Wed, 13 May 2026 00:17:22 GMT  
		Size: 138.1 MB (138068535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852435ea145d7d7594f9a4ab92e94ae4f3c2754ac0f123535258a464ec70892c`  
		Last Modified: Wed, 13 May 2026 00:17:18 GMT  
		Size: 35.0 KB (35012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:ac1471d2ae9a89c537c20d9b56b1f2c4338c622d11d94f723d266092cc834ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d92dae32559ea014f961fd5a20a8ea5daafe11e06120af7658dfe5b578f60f0`

```dockerfile
```

-	Layers:
	-	`sha256:19638ac92549a7cdf8751f1bb8cb7be2ef6e7a3afc1a14bba8df4b26b62d00c9`  
		Last Modified: Wed, 13 May 2026 00:17:18 GMT  
		Size: 5.5 MB (5523440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e00757b85eb8b4d633744aadfc23aa91c3042484918640d83bcc9fcde9c3ec`  
		Last Modified: Wed, 13 May 2026 00:17:18 GMT  
		Size: 24.5 KB (24527 bytes)  
		MIME: application/vnd.in-toto+json
