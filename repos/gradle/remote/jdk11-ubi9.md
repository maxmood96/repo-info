## `gradle:jdk11-ubi9`

```console
$ docker pull gradle@sha256:084229f2fcec89c4843878ba2cbf87a799eb835beae1082c855b0df6eb03b8f4
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

### `gradle:jdk11-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:3c1bf35d765cf756e6718e7f87bcfacc3315805dc4aea0087c7101965948950e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.3 MB (387286836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526e647d8c67a8740fb0743e52c4514ee4c6137c6d068361e27e6b06ca7d0037`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:27:16 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:27:16 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:27:16 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:27:16 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:27:17 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:27:17 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:27:17 GMT
ENV container oci
# Mon, 04 May 2026 01:27:17 GMT
COPY dir:65829633e0a732ee03a3da731062eca14df67dc0e6bab86d02002ef9d123d97c in /      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:27:17 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:27:17 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
COPY file:c2149fceb878782b97b2875047824d21e0e5ecd57a50bf8e1dd5d47550f18358 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:27:18 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:27:05Z" "org.opencontainers.image.created"="2026-05-04T01:27:05Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:27:05Z
# Tue, 05 May 2026 23:08:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:13 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 05 May 2026 23:08:19 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:21 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:11:53 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:11:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:11:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:11:53 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:11:53 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:11:59 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:11:59 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 06 May 2026 00:11:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 06 May 2026 00:12:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:12:01 GMT
USER gradle
# Wed, 06 May 2026 00:12:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 May 2026 00:12:01 GMT
USER root
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51161c23a7e1e1c57a03bf92078d59e0a18e67ee2b41dc3ec7f90535e5d953e`  
		Last Modified: Tue, 05 May 2026 23:08:36 GMT  
		Size: 16.2 MB (16237771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d64eec189d5e0b536d3648756f234b56c2e42360f4fc015e695c783662752d`  
		Last Modified: Tue, 05 May 2026 23:08:39 GMT  
		Size: 142.3 MB (142348905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba40824cca877b43a7567967a4cdac1f7f3d9e9119bb11b2acb31dd7a85478`  
		Last Modified: Tue, 05 May 2026 23:08:35 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab17b341c0be7c9774e8799edfc8d6c007457e7550e1767b15a3941087e97b5`  
		Last Modified: Tue, 05 May 2026 23:08:35 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef943fca1b1d499200a1384058c8fb76da16b7a70b233e304060fdc64c18dee`  
		Last Modified: Wed, 06 May 2026 00:12:18 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc027e65c422bd50ae217338a340555b7691bf45dafe61e4295bce11dc39a3b7`  
		Last Modified: Wed, 06 May 2026 00:12:21 GMT  
		Size: 51.2 MB (51234005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c34b77df6ae0ae88402363aef7a2feb01b65c77f6340e6bb50d7592bfc32b69`  
		Last Modified: Wed, 06 May 2026 00:12:23 GMT  
		Size: 137.4 MB (137388271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9400024c63454eb190e860e6bdaf496c4d9cf751659e39b6ad8eb4ef584f11`  
		Last Modified: Wed, 06 May 2026 00:12:18 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:3ad0f7d6c62f479439bcc65d6f460dc8f8e60656139ac6f2da052cc96e6c7544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b028ffc9a7484ef46f82648369dd1e1ba01fe780211238a58055d6567d8698`

```dockerfile
```

-	Layers:
	-	`sha256:2f5efdd0794765c652b80afaaf070d6bda2b64569cead05a4171afa3247f8c4d`  
		Last Modified: Wed, 06 May 2026 00:12:18 GMT  
		Size: 5.4 MB (5426457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7596a44d5870938392950485cc6a474b67a79e192c55d48c926835ae21de997e`  
		Last Modified: Wed, 06 May 2026 00:12:18 GMT  
		Size: 24.2 KB (24167 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:47c46fde5b5edae4f4285f02268dbb67e45caa36aed575d1ac0db054905ee6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381906168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bae4f03b989a5e586fb761c1d4d24972fcda10d2131e94e91571470e52c84d3`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:30:08 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:08 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:08 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:08 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:08 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:08 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:08 GMT
ENV container oci
# Mon, 04 May 2026 01:30:09 GMT
COPY dir:5ad712b8248d48b2932fa5bdcc0ad50ec37c7d49fe231a7db1a1c2391217329a in /      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:09 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:09 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
COPY file:11a91ebd5ef22e4f28676b4a9dc8447f7af7f01609b0311ebd76ca9c6631f340 in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:10 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:29:56Z" "org.opencontainers.image.created"="2026-05-04T01:29:56Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:29:56Z
# Tue, 05 May 2026 23:07:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:07:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:07:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:07:50 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:07:50 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 05 May 2026 23:07:57 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:07:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:07:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:07:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:07:59 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:12:34 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:12:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:12:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:12:34 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:12:34 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:12:40 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:12:40 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 06 May 2026 00:12:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 06 May 2026 00:12:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:12:42 GMT
USER gradle
# Wed, 06 May 2026 00:12:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 May 2026 00:12:43 GMT
USER root
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59c9682fe91a77ac081707e04b134c8ee8b37f9fe90356c8ae8886ffe8cd581`  
		Last Modified: Tue, 05 May 2026 23:08:14 GMT  
		Size: 16.8 MB (16767565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b6b213b2e152e3b0d022941f66e5336ca9fdedffd6dac8ee69923847949e1`  
		Last Modified: Tue, 05 May 2026 23:08:17 GMT  
		Size: 139.0 MB (139040652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade07814c49b1a26f6f4ed5e69c62d65eac7bd39746b58418e8ec871cc5aeeb6`  
		Last Modified: Tue, 05 May 2026 23:08:14 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f785cb528118cef121b68c6b93061218a232ceb0cfbfca81578f3210c0a8231`  
		Last Modified: Tue, 05 May 2026 23:08:14 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82c9fdf99c188590a60d66d16fd64d170ec4026f3c527f04ceefe801f56fe08e`  
		Last Modified: Wed, 06 May 2026 00:13:00 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0119a8619e613c6187f18425133b7143a9cacb78647ee7e7c44621a05b4b566`  
		Last Modified: Wed, 06 May 2026 00:13:03 GMT  
		Size: 50.4 MB (50440462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cbbfe0ce6edd4ea00b6c0f59ba6788ae38ddc5e8cd7a8f567d15a00b7175e1`  
		Last Modified: Wed, 06 May 2026 00:13:06 GMT  
		Size: 137.4 MB (137388273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90e1fcf433714e465d99a96ef816a1c5764754a9fc2bce501e85c9591f96833`  
		Last Modified: Wed, 06 May 2026 00:13:01 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:f1d6c3a84812abf49b3221bcb820c13b00915f72713a5c067054f5e92f5b5bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41053e3c4074a8a76c09f46d38ae1cb6124de65070672f8d8949a18081226108`

```dockerfile
```

-	Layers:
	-	`sha256:ebfca0364b19be5d4d547d526b50bbdace7a3923aa7b8cb190979a7a9b4dab09`  
		Last Modified: Wed, 06 May 2026 00:13:00 GMT  
		Size: 5.4 MB (5426505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a3c91c8c21769460ca29a0865ef8607759ce205a9077a8ce51265a6174b151`  
		Last Modified: Wed, 06 May 2026 00:13:00 GMT  
		Size: 24.4 KB (24364 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:d51f0ed207d180b85b6021137908c732ff676f9b73508b96106ae99cb7a81534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.7 MB (382741394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fbeda6e9d2d4e12026f37928a4b3b6b85f06f7b017ee18faeb43c2efb6e25e`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:28:51 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:28:51 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:28:51 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:28:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:28:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:28:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:28:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:28:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:28:52 GMT
ENV container oci
# Mon, 04 May 2026 01:28:52 GMT
COPY dir:95ecb7253fddf635ae6d975427ddb73b0a49c785b217cf296b0a0358678fc43f in /      
# Mon, 04 May 2026 01:28:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:28:52 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:28:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:28:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:28:53 GMT
COPY file:21c41e3d00d3a684fc39637052cae774dab908d634556245b0fd07fa3273162a in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:28:53 GMT
COPY file:21c41e3d00d3a684fc39637052cae774dab908d634556245b0fd07fa3273162a in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:28:53 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:28:41Z" "org.opencontainers.image.created"="2026-05-04T01:28:41Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:28:41Z
# Tue, 05 May 2026 23:48:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:48:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:48:45 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:48:45 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 05 May 2026 23:50:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:50:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:50:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:50:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:50:39 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:21:45 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:21:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:21:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:21:45 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:21:46 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:22:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:22:08 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 06 May 2026 00:22:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 06 May 2026 00:22:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:22:13 GMT
USER gradle
# Wed, 06 May 2026 00:22:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 May 2026 00:22:17 GMT
USER root
```

-	Layers:
	-	`sha256:651dc6a385386e8e87790c18da9695023b6028435c56101235d26c0359b72932`  
		Last Modified: Mon, 04 May 2026 06:11:22 GMT  
		Size: 44.4 MB (44437692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1767d5eb85065ec07c318883803129ba6d9958ad6e2956b0bc74061b3eaad718`  
		Last Modified: Tue, 05 May 2026 23:49:22 GMT  
		Size: 17.9 MB (17908683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d71fcf9e24c2215c28aabdc0a597985c76ead273006f75b456550307a5814e`  
		Last Modified: Tue, 05 May 2026 23:51:22 GMT  
		Size: 129.6 MB (129614168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60d41dc7948debbe598bee3eb031d4aabf5faf80cdd6bfdf5189494d9d7e3c`  
		Last Modified: Tue, 05 May 2026 23:51:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f24b43c09f7806f4c5cf410e94b4abd0860190c9f5f90fa111fddbe58886024`  
		Last Modified: Tue, 05 May 2026 23:51:18 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ef59a587342e92fb884b31f1cf9f707776bc56faa552c1f8a53c3529dfa44a`  
		Last Modified: Wed, 06 May 2026 00:22:53 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97386877058bf83b1538b096366b6225e3137a6ccc8f9185869fad271a9789ef`  
		Last Modified: Wed, 06 May 2026 00:22:56 GMT  
		Size: 53.4 MB (53353689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdeff60dc02b14b1d2eb7cf92cc990dbb87a7c0ebd9a3bb1a0e4a5f1eb1d4ec`  
		Last Modified: Wed, 06 May 2026 00:23:03 GMT  
		Size: 137.4 MB (137388277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7b9fe79bd3b47e1c9d94d4028d890b6be18ed5076a1c9d1d02793566396f1f`  
		Last Modified: Wed, 06 May 2026 00:22:53 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:5d6dd0db7fb85a483e9334f7edce32d34855a23bad39d52a2ffec9938a301f1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5447454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e1f7e5c41736255f76b1ed4953fbb5f57792c8f19df3184857d3692ebc4358`

```dockerfile
```

-	Layers:
	-	`sha256:85cbb63aecd519f9db99bd1e1dbd9421dd4c928298b97dc11b8117cdebe379ee`  
		Last Modified: Wed, 06 May 2026 00:22:53 GMT  
		Size: 5.4 MB (5423177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1c1ca34f6cc674cc4e121d2435d5d1ddbbd3a37148f0210301b0d9948db18e7`  
		Last Modified: Wed, 06 May 2026 00:22:53 GMT  
		Size: 24.3 KB (24277 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:375f6cd831afcdf475e6571b30c4a882db86ca68722255b45bf2ac5ba5c64e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365725577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f690a1c6ec0eb5d8df6e641d99612fab649d95a1a8e341b5149ec319592ba1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 01:30:44 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 04 May 2026 01:30:44 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 04 May 2026 01:30:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 04 May 2026 01:30:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 04 May 2026 01:30:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 04 May 2026 01:30:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 04 May 2026 01:30:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 04 May 2026 01:30:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 04 May 2026 01:30:44 GMT
LABEL io.openshift.expose-services=""
# Mon, 04 May 2026 01:30:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 04 May 2026 01:30:44 GMT
ENV container oci
# Mon, 04 May 2026 01:30:45 GMT
COPY dir:76ee59d0cc4ac3b25df131d5b792de0ca9dea076f16b0a8067e3fa28fe221dca in /      
# Mon, 04 May 2026 01:30:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 04 May 2026 01:30:45 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 01:30:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 04 May 2026 01:30:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 04 May 2026 01:30:45 GMT
COPY file:8117a8affdbadf4490ec3e7805362a99c6b7c4323cce49231cefc73404cbdb1e in /usr/share/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:45 GMT
COPY file:8117a8affdbadf4490ec3e7805362a99c6b7c4323cce49231cefc73404cbdb1e in /root/buildinfo/labels.json      
# Mon, 04 May 2026 01:30:45 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "org.opencontainers.image.revision"="dbf428e1775c5e4c4802b4c714d3b50b652d0c8a" "build-date"="2026-05-04T01:30:21Z" "org.opencontainers.image.created"="2026-05-04T01:30:21Z" "release"="1777857961"org.opencontainers.image.revision=dbf428e1775c5e4c4802b4c714d3b50b652d0c8a,org.opencontainers.image.created=2026-05-04T01:30:21Z
# Wed, 06 May 2026 00:08:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 May 2026 00:08:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 May 2026 00:08:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 May 2026 00:08:38 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 06 May 2026 00:08:38 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 06 May 2026 00:08:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 06 May 2026 00:08:46 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 06 May 2026 00:08:46 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 06 May 2026 00:08:46 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 06 May 2026 00:08:46 GMT
CMD ["jshell"]
# Wed, 06 May 2026 01:14:13 GMT
CMD ["gradle"]
# Wed, 06 May 2026 01:14:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 01:14:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 01:14:13 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 01:14:13 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 01:14:18 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 01:14:18 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 06 May 2026 01:14:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 06 May 2026 01:14:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 01:14:21 GMT
USER gradle
# Wed, 06 May 2026 01:14:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 May 2026 01:14:22 GMT
USER root
```

-	Layers:
	-	`sha256:d2d3d6ef96ac4ab8b8476f11203d7d0f260d5b69f1707977e64f156a31c19587`  
		Last Modified: Mon, 04 May 2026 06:11:15 GMT  
		Size: 38.1 MB (38127952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5afa710876084c876576949ddf614830c05094fdaabca4ddecf0cfc67c96da`  
		Last Modified: Wed, 06 May 2026 00:09:18 GMT  
		Size: 16.6 MB (16596573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706c05b62ca0d9e436a75c1131476a4a2498b5e6586ffe0f61eb487b468cca49`  
		Last Modified: Wed, 06 May 2026 00:09:20 GMT  
		Size: 123.1 MB (123061417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f84a48cf43c928134e6e29e5f447a4096b2091cd2e7a3f36c0ef4c7e7f94b77`  
		Last Modified: Wed, 06 May 2026 00:09:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd8b95c45aa78f17a79e6d194a47e99155de44e75ea67708376c1013e4a98d0`  
		Last Modified: Wed, 06 May 2026 00:09:18 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c894da8782899423bf78f4abd0cc5e26cfdf158a1d312a3dbb9f2e797e34188f`  
		Last Modified: Wed, 06 May 2026 01:14:59 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18baf27776608771bc7c183241e50278ef0ce8966630e29cda02882e9c46991e`  
		Last Modified: Wed, 06 May 2026 01:15:00 GMT  
		Size: 50.5 MB (50512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977dce83170ba78d61e88f10155655fb47fa63786e100fed4daceedc14fa08eb`  
		Last Modified: Wed, 06 May 2026 01:15:02 GMT  
		Size: 137.4 MB (137388297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3f4b9a700617c9caf865445f89a71da8eced5ac4e48eb938b7f5f34332a90d`  
		Last Modified: Wed, 06 May 2026 01:14:59 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:fac621754972f769a900c3a556e072e924245376bf0655942ce42c790592a6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f490ec4de97047cb65e0df96156869874424c04a276b25e64439bc4d67095f5`

```dockerfile
```

-	Layers:
	-	`sha256:89792670bc8f6e26a4fc0be3c0fafe41117fcbb1ae94b018d579a9a55b9b384b`  
		Last Modified: Wed, 06 May 2026 01:14:59 GMT  
		Size: 5.4 MB (5413066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5c926917959b2009dbf0b7c2d15befd84a9a2f9112f002c0a4c8b256b7d9be9`  
		Last Modified: Wed, 06 May 2026 01:14:59 GMT  
		Size: 24.2 KB (24203 bytes)  
		MIME: application/vnd.in-toto+json
