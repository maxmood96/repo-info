## `gradle:9-jdk26-ubi10`

```console
$ docker pull gradle@sha256:3af9724a4d95610609134f343dda858299962dd3e786721eec34890582d4f56c
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

### `gradle:9-jdk26-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:f66207bc98ce5a35e2fd2f705b4a443a5bf2e282ce1f060cfb875afb964e2ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347672212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0b9b817197c01b60c4827b3aaf01b9363c2959f3cb36091f5f73fd65817587`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:40:14 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:40:14 GMT
ENV container oci
# Wed, 24 Jun 2026 06:40:14 GMT
COPY dir:92709e786f8e662d73459e8ec6b629a535dce92ae9fcad21b6d7b00ac6803604 in /      
# Wed, 24 Jun 2026 06:40:14 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:40:14 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:40:14 GMT
COPY dir:e8e2b7cb869a17d32d7452a63fca2737847da7b62b5d0406fabbac5267964ccc in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:40:15 GMT
COPY dir:e8e2b7cb869a17d32d7452a63fca2737847da7b62b5d0406fabbac5267964ccc in /root/buildinfo/      
# Wed, 24 Jun 2026 06:40:15 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:39:51Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:39:51Z" "architecture"="x86_64" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:39:51Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:04:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:04:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:04:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:04:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:04:50 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Wed, 24 Jun 2026 23:04:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:04:58 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:04:58 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:04:58 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:04:58 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:14:04 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:14:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:14:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:14:04 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:14:04 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:07 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:07 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:10 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:11 GMT
USER root
```

-	Layers:
	-	`sha256:d16bd660d5aff2d8cb434aefeedc41e2a96fcbfce0e10b612181d05ae773b985`  
		Last Modified: Wed, 24 Jun 2026 09:11:20 GMT  
		Size: 34.9 MB (34866797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d657ab9f95e018acb6ba5777602c3c0d0303469b90c730c6e67c95d716026b0d`  
		Last Modified: Wed, 24 Jun 2026 23:05:17 GMT  
		Size: 37.8 MB (37775788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01528a95db6b557b269590271534f2db74238b27b2b988fe5423037c7ad8ac48`  
		Last Modified: Wed, 24 Jun 2026 23:05:18 GMT  
		Size: 94.5 MB (94525388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1286933a5a6bbb3442b8318e22ba115f2d2f9a384fb5577be9841670df36a2a5`  
		Last Modified: Wed, 24 Jun 2026 23:05:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af57834c53a50bff3053e382c7d15143696af5a5ad163a512343c0f5758eae7a`  
		Last Modified: Wed, 24 Jun 2026 23:05:15 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915d7b1cc68368cfcc255d356d9015db12074f631d813b34a142a529d620d28c`  
		Last Modified: Mon, 29 Jun 2026 17:14:30 GMT  
		Size: 1.6 KB (1591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85038052301d45e8aaca10e8d8ee363daa50b5a637abdf26022fd865198f66b`  
		Last Modified: Mon, 29 Jun 2026 17:14:31 GMT  
		Size: 39.9 MB (39878375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ca53cf009175e2c40ea3ae1567f889efcb2587ec06e7af9ee36171be7d9353`  
		Last Modified: Mon, 29 Jun 2026 17:14:34 GMT  
		Size: 140.6 MB (140596026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d63c458c14f6e8bcea5930d6961381fd5be93db31b8011d3f3ef1f7f47f1ad9`  
		Last Modified: Mon, 29 Jun 2026 17:14:30 GMT  
		Size: 25.6 KB (25616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:1f5479451d7dd89cc06810df43d39307cfaf537cfe77cbdd29a430112f939e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7077920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7299f48f9b882548d0440de0111dc8133dc843d80747a010c5085630ffb9e6c1`

```dockerfile
```

-	Layers:
	-	`sha256:16849285efd0a82becf4b4cfa00d5d3200da775063259e3ea6d88b6e97d52309`  
		Last Modified: Mon, 29 Jun 2026 17:14:30 GMT  
		Size: 7.1 MB (7053499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834ef31244b9f965f93f43e5a3d6158a7d2080fd40c5b4b6dbe7f79c01df7da1`  
		Last Modified: Mon, 29 Jun 2026 17:14:29 GMT  
		Size: 24.4 KB (24421 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a746dbbf4745e9b62963f866784d5b8fbd6ea1a0fdb59815cdcdbbc9e9b4730b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.2 MB (344218802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b3f8a53020c46b7fbb2e1c7469f8d05763729dfc6dccfad6b577cc6201b8fff`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:17 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:45:18 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:45:18 GMT
ENV container oci
# Wed, 24 Jun 2026 06:45:18 GMT
COPY dir:0b29f9e66bf048f7202a79e2f728b8f136d2a972d39ff75508b0f9653d433ed0 in /      
# Wed, 24 Jun 2026 06:45:18 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:45:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:45:19 GMT
COPY dir:1852be49c9caac8615951d68388d7f8791140b539cc11bfda91b044119d75a5d in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:45:19 GMT
COPY dir:1852be49c9caac8615951d68388d7f8791140b539cc11bfda91b044119d75a5d in /root/buildinfo/      
# Wed, 24 Jun 2026 06:45:19 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:44:57Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:44:57Z" "architecture"="aarch64" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:44:57Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:03:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:03:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:03:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:03:17 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:03:17 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Wed, 24 Jun 2026 23:03:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:03:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:03:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:03:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:03:50 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:14:01 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:14:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:14:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:14:01 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:14:01 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:05 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:08 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:09 GMT
USER root
```

-	Layers:
	-	`sha256:6bcf33c78aa091990500f016c1ed0cb35bc3f67461b918afc9de35f0b601382c`  
		Last Modified: Wed, 24 Jun 2026 09:11:21 GMT  
		Size: 33.0 MB (33046417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefc97f25d8e3d980a7a9475955b9d9face593a9a4d811eafca4ebcf20954a13`  
		Last Modified: Wed, 24 Jun 2026 23:03:35 GMT  
		Size: 37.7 MB (37712457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2ee52e6bb62bbfd29fcd60d579523503b7b662eabd08d3fc6161994da594b7`  
		Last Modified: Wed, 24 Jun 2026 23:04:09 GMT  
		Size: 93.5 MB (93505311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea96c806f7db5cde40f5fcd85273a0df4152eb2c4cc6f35c4062c5317bb54db`  
		Last Modified: Wed, 24 Jun 2026 23:04:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026ddc256c6a890c3d031516bb9630d85c93574f1bac27fd3977e89c71d94e14`  
		Last Modified: Wed, 24 Jun 2026 23:04:07 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41cd183850dd83fc7e4ec38e65678a9362fb9bb9d38a1a8b3d72a2febe3cc14`  
		Last Modified: Mon, 29 Jun 2026 17:14:28 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3923ba7f9799e7ee70de628a7d81f0a1cc19ce6f2942a2153ac2731936b4871`  
		Last Modified: Mon, 29 Jun 2026 17:14:30 GMT  
		Size: 39.3 MB (39325015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52610d2326b89340fb8194d1bdc5db91a97f017011b5017928eeecfea9f5ba04`  
		Last Modified: Mon, 29 Jun 2026 17:14:32 GMT  
		Size: 140.6 MB (140596028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b019150403ae2b4280fb2e0392c95a94c1a5baf93b3af036b951cd1c8bf3111f`  
		Last Modified: Mon, 29 Jun 2026 17:14:28 GMT  
		Size: 29.3 KB (29348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:474ded5b5d35eb495c2b987215d571c05ae839162370677a5c747aa85dae2472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7076370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13e017d549fb8d5493ec2b09d6e08eb1b5dbad46578ea30a9a2b96c7c32bef9`

```dockerfile
```

-	Layers:
	-	`sha256:d04786696b09757ad7fb2f25cefc7b25314866c0590f6dff4d286ac9dbc8df8a`  
		Last Modified: Mon, 29 Jun 2026 17:14:28 GMT  
		Size: 7.1 MB (7051752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf3bcf832e0cb461604b2a6716ccb20b5ef9b0198c885bd336f4f546666df0c`  
		Last Modified: Mon, 29 Jun 2026 17:14:28 GMT  
		Size: 24.6 KB (24618 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:e97c29bedc76f5fd81fe5ab58572d72c757d0155c708a03f3048ad9a9ad14010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354679172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4515d48a8353a66610a8b3343a6a562ebb952a4e53c82547d1eb41156bbae0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:45:06 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:45:06 GMT
ENV container oci
# Wed, 24 Jun 2026 06:45:06 GMT
COPY dir:edae26e2804200dda741354aeaa508164e0f6589abbc418ddf0174c7e9c74460 in /      
# Wed, 24 Jun 2026 06:45:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:45:06 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:45:06 GMT
COPY dir:4159190efbf3bf817f31486123f361d6a5105b0e524913dcf5088003851d564d in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:45:06 GMT
COPY dir:4159190efbf3bf817f31486123f361d6a5105b0e524913dcf5088003851d564d in /root/buildinfo/      
# Wed, 24 Jun 2026 06:45:07 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:44:49Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:44:49Z" "architecture"="ppc64le" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:44:49Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:02:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:02:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:02:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:02:02 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:02:02 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Wed, 24 Jun 2026 23:10:40 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:10:44 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:10:55 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:10:55 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:10:55 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:22:20 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:22:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:22:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:22:20 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:22:20 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:22:38 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:22:38 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:22:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:22:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:22:43 GMT
USER gradle
# Mon, 29 Jun 2026 17:22:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:22:45 GMT
USER root
```

-	Layers:
	-	`sha256:c0e83bd19bb537d0b48ac2365b13cdff44e889f5083fbf4be3569d1b4825377d`  
		Last Modified: Wed, 24 Jun 2026 12:17:52 GMT  
		Size: 39.0 MB (39004054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86309525b0d7959e843b2d2b23c4513e7ab084fa30bba69cb7f4566f4379eb6`  
		Last Modified: Wed, 24 Jun 2026 23:02:38 GMT  
		Size: 39.5 MB (39527160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbfefac311abe23ddc934477a47b7366f0c4f08db039787a6d3ef750a3d4183`  
		Last Modified: Wed, 24 Jun 2026 23:11:30 GMT  
		Size: 93.9 MB (93902368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73b6ffbea767273195f6749b72663e0b803637ba4a8282b63ff2d80a8df50c6`  
		Last Modified: Wed, 24 Jun 2026 23:11:27 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3958a505e241c3309aacf3eef70b2036964621f9a61b51c8d334aa5a44091fd`  
		Last Modified: Wed, 24 Jun 2026 23:11:27 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ddd53dc93649af0e11771b9096c04b856075f74f4c48b605d763d3f64e4a60`  
		Last Modified: Mon, 29 Jun 2026 17:23:34 GMT  
		Size: 1.6 KB (1591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f52b8b5b0b694d43629ba282394d07665f980570696aa5c4069b5d86c58fd`  
		Last Modified: Mon, 29 Jun 2026 17:23:36 GMT  
		Size: 41.6 MB (41644965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946836cf4ca56b01132547c55e3ed9de1976d41e048310252732c90640f01de8`  
		Last Modified: Mon, 29 Jun 2026 17:23:38 GMT  
		Size: 140.6 MB (140596027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c46bebd048550d722100ee4be6e1cff99bbae626f75cea2f063e46c48386d9`  
		Last Modified: Mon, 29 Jun 2026 17:23:34 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:268cd4a18e8299d2a951571d914f3a659cef73e5e269b5d46031cd8f9991e837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7053346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9ab1d4828a838f04d21cbd1ad53060c0ba3f06c942648e5110c3d4a424370d`

```dockerfile
```

-	Layers:
	-	`sha256:729d1cd656473d94a86189a8f77e73e998b2db52e5eb7d8c97660698670008da`  
		Last Modified: Mon, 29 Jun 2026 17:23:34 GMT  
		Size: 7.0 MB (7028853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de7c71dbe1232a04b86259a8fcec95f9ba7390c2c3c705a9958098234cf5703`  
		Last Modified: Mon, 29 Jun 2026 17:23:34 GMT  
		Size: 24.5 KB (24493 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:6a268a456e19b90aeab772d89308a7f9477678f0a0e689461b10aadab4802a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346056017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5678668d49b4a695aa517a36b83666b56caf8e8d50b0c2b2d34016d3d4fcf120`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL io.openshift.expose-services=""
# Wed, 24 Jun 2026 06:50:01 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 24 Jun 2026 06:50:01 GMT
ENV container oci
# Wed, 24 Jun 2026 06:50:02 GMT
COPY dir:44a98658e38dbd3fe1a481ca6dd5239f51de526a3f13e8e4aae2600c0e195400 in /      
# Wed, 24 Jun 2026 06:50:02 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 24 Jun 2026 06:50:02 GMT
CMD ["/bin/bash"]
# Wed, 24 Jun 2026 06:50:02 GMT
COPY dir:faeaf738fafa5618598acb30c3f03d041d09c185c5e2d603c791711084b47697 in /usr/share/buildinfo/      
# Wed, 24 Jun 2026 06:50:02 GMT
COPY dir:faeaf738fafa5618598acb30c3f03d041d09c185c5e2d603c791711084b47697 in /root/buildinfo/      
# Wed, 24 Jun 2026 06:50:02 GMT
LABEL "org.opencontainers.image.created"="2026-06-24T06:48:38Z" "org.opencontainers.image.revision"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "build-date"="2026-06-24T06:48:38Z" "architecture"="s390x" "vcs-ref"="fcffc2222455e28601e0105a0a1e9a211f7127c7" "vcs-type"="git" "release"="1782283038"org.opencontainers.image.created=2026-06-24T06:48:38Z,org.opencontainers.image.revision=fcffc2222455e28601e0105a0a1e9a211f7127c7
# Wed, 24 Jun 2026 23:01:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 23:01:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 23:01:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jun 2026 23:01:58 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 24 Jun 2026 23:01:58 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Wed, 24 Jun 2026 23:04:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='613f9b2861dea937b24d5eca745ef8567733b377d0bb612195acaad0e3f61360';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_aarch64_linux_hotspot_26.0.1_8.tar.gz';          ;;        ppc64le)          ESUM='60e016faf4177840430035d948f83f2887d556fe512b78c1d43b320322fe6685';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_ppc64le_linux_hotspot_26.0.1_8.tar.gz';          ;;        s390x)          ESUM='942de7ded1427592a2a4b6dbea4083b2d0891de2626c7863e970de3e2819a93f';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_s390x_linux_hotspot_26.0.1_8.tar.gz';          ;;        x86_64)          ESUM='8e512f13e575a43655fc92319436c94890c137b9035cc6bd6f9cf24239704d3a';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26.0.1%2B8/OpenJDK26U-jdk_x64_linux_hotspot_26.0.1_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 24 Jun 2026 23:04:13 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jun 2026 23:04:13 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jun 2026 23:04:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jun 2026 23:04:13 GMT
CMD ["jshell"]
# Mon, 29 Jun 2026 17:13:24 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:24 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:24 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:29 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:33 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:34 GMT
USER root
```

-	Layers:
	-	`sha256:f8130189e85e92c4ff7cc258627f77e071b689832e41f79f26767374d60fb4c3`  
		Last Modified: Wed, 24 Jun 2026 12:17:47 GMT  
		Size: 34.8 MB (34775089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e258a83fe70f2f168f5b4f2b3184cba856f596dee52b05bdf5b1eb5bfdc3d32`  
		Last Modified: Wed, 24 Jun 2026 23:02:28 GMT  
		Size: 38.2 MB (38150217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576b0ce215a470fa9ca5c7a90d77d4c7058f6bd2671d895be75eab1e13c928df`  
		Last Modified: Wed, 24 Jun 2026 23:04:40 GMT  
		Size: 90.5 MB (90537370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b497f0139ee326f26be622d0e4ba68610c36ce98524c40f6091e4431f1d7df5`  
		Last Modified: Wed, 24 Jun 2026 23:04:37 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef025080aa2c65748d4708454da7c3c0eb5ef8cc6162401c029fa63ce99dfc6`  
		Last Modified: Wed, 24 Jun 2026 23:04:37 GMT  
		Size: 2.5 KB (2471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486c24c7df56b21dd375a05fda16d3c6a905dcec46fac99c6fe5e830d12605f1`  
		Last Modified: Mon, 29 Jun 2026 17:14:04 GMT  
		Size: 1.6 KB (1591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da41ec2fa42fb3f8e69410f1f09a4d89cbf0799c2b020d193a3866ef208cd541`  
		Last Modified: Mon, 29 Jun 2026 17:14:05 GMT  
		Size: 42.0 MB (41992711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c18c1714bb2f1a41a002a8c676bf21692cbb404435680707f907f5b6513c33`  
		Last Modified: Mon, 29 Jun 2026 17:14:07 GMT  
		Size: 140.6 MB (140596032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b8d7b04e115438d5c9c400cd65789e203d905d399e27a9e60a795405932752`  
		Last Modified: Mon, 29 Jun 2026 17:14:04 GMT  
		Size: 375.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:ad73415c580071b4cabfd02b9939a14da6c0496a6580e183045094b3dd48b34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7043751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b1e48ecafa7647830d898cc88550e85c874416baf2775cbfaae2b300ab84ab`

```dockerfile
```

-	Layers:
	-	`sha256:5ec4f93f14643641820014da9b78aa8ce9f55ef198fa777d0dd03c82e2398d20`  
		Last Modified: Mon, 29 Jun 2026 17:14:04 GMT  
		Size: 7.0 MB (7019332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd79c1c42b16bf73fce4955071f6c6acf23cf7bc001be15e7d6440fa14adddd8`  
		Last Modified: Mon, 29 Jun 2026 17:14:04 GMT  
		Size: 24.4 KB (24419 bytes)  
		MIME: application/vnd.in-toto+json
