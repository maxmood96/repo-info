## `gradle:9-jdk17-ubi9`

```console
$ docker pull gradle@sha256:55eb6f63d71d5f3f019dbb382ed6167d2e7a0c7539f0f82fd122e8c01df8879f
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

### `gradle:9-jdk17-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:bdb53379bf2e01ed6852f941ba763d18875bfc653dae7c69b26596d3e9b8d94e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 MB (393393588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9dca641f111c6e36a799382872ea0bebaa1a5af5fe399e6178a231a5bcbe311`
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
# Tue, 05 May 2026 23:08:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:22 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:22 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 05 May 2026 23:08:28 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:29 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:29 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:29 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:12:03 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:12:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:12:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:12:03 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:12:03 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:12:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:12:08 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 00:12:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Wed, 06 May 2026 00:12:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:12:11 GMT
USER gradle
# Wed, 06 May 2026 00:12:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 06 May 2026 00:12:11 GMT
USER root
```

-	Layers:
	-	`sha256:cd8d59cb7a894fbcbefe70d3cdbc433492e715351e24e77b24a441609ab2de47`  
		Last Modified: Mon, 04 May 2026 03:52:20 GMT  
		Size: 40.0 MB (40019116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd29c8bfda7c60b7a0cfd50de480ba2b6d27bd992b6133397b42fc3aa3ab104`  
		Last Modified: Tue, 05 May 2026 23:08:46 GMT  
		Size: 16.2 MB (16237620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240aea9e43ff099486c3dbedccd03e011ff2da3b837640838c10ac7c1c5218b7`  
		Last Modified: Tue, 05 May 2026 23:08:49 GMT  
		Size: 145.6 MB (145637103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fbfe8da4353d3ab339085e891bdadb36dd706486157bf917b0997ad69635dc`  
		Last Modified: Tue, 05 May 2026 23:08:45 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e987ddb28ab58101424545972ffd0bbbf0333cec9348b32b02b187092d5b72e`  
		Last Modified: Tue, 05 May 2026 23:08:45 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82beff65545a8ae6ab12949ccdd8c7674190e7a9600f752b081fabc6b81fb54d`  
		Last Modified: Wed, 06 May 2026 00:12:28 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdc9b0d4ba91dbea5881c5f78d972d6c538c5b81fc4b1ae532154bc67782819`  
		Last Modified: Wed, 06 May 2026 00:12:30 GMT  
		Size: 51.2 MB (51234326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6f8797725a2a2b0e37b3acca246d6559ea065c460ef274dae0df1dfcb1cd08`  
		Last Modified: Wed, 06 May 2026 00:12:32 GMT  
		Size: 140.2 MB (140235940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073ef5bcbc6ccb2621e9490668f5308bd18dc56bce70bd6461838326c65202c`  
		Last Modified: Wed, 06 May 2026 00:12:28 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:472d97ad27180ca0952c4e0a36f9fe1a9a32e993a96412a45689297598353e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb119a0bc2d57d2687a375be64c61d886320e4aed5faf80d4dd063bcb10e2a31`

```dockerfile
```

-	Layers:
	-	`sha256:36932cd3dbf4cde0c22107f22c4b2d718a896cc02b3e9a455d0d4312f9785c33`  
		Last Modified: Wed, 06 May 2026 00:12:28 GMT  
		Size: 5.4 MB (5420369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2cd183bd5db9cff0db25a15af86dcf403437d495030e2798bc26d9f2f677ad8`  
		Last Modified: Wed, 06 May 2026 00:12:28 GMT  
		Size: 23.2 KB (23196 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e18897d54adf5d5b4f9e1529afea4504ff672a42cc0ce78babec55feb546ba54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.1 MB (390129669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28fbd20805136949a0301e9c1757640e6ee796b2d8e6369aa9fa5b1886c9ac36`
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
# Tue, 05 May 2026 23:08:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 05 May 2026 23:08:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 May 2026 23:08:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 May 2026 23:08:10 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 05 May 2026 23:08:10 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 05 May 2026 23:08:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:08:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:08:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:08:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:08:18 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:12:14 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:12:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:12:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:12:14 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:12:14 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:12:20 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:12:20 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 00:12:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Wed, 06 May 2026 00:12:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:12:24 GMT
USER gradle
# Wed, 06 May 2026 00:12:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 06 May 2026 00:12:25 GMT
USER root
```

-	Layers:
	-	`sha256:eae0b4c39ea6d65927abe502bd11bbd574acc09733cb468c989628c5b204a24b`  
		Last Modified: Mon, 04 May 2026 05:13:02 GMT  
		Size: 38.2 MB (38205818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3563564b5b0ce572db0cb7c2be1b3431521f73e875045af458e783b2256db59e`  
		Last Modified: Tue, 05 May 2026 23:08:35 GMT  
		Size: 16.8 MB (16767606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1f50324cb988907647f459c56fa43db31412b5199ed01360db5026296ecada`  
		Last Modified: Tue, 05 May 2026 23:08:38 GMT  
		Size: 144.4 MB (144446555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461882e9f5175679cb3956772f7894b1f55c3f9a7c2641f8ff8f44989cfe9d97`  
		Last Modified: Tue, 05 May 2026 23:08:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d0cc7cdf52f20313dc270fbd795afef19b7d68114e48dd7051a53a4338dfa4`  
		Last Modified: Tue, 05 May 2026 23:08:34 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6417d8ddb8aae8e9584a1eff101d3c3be1b2fd25a7dddc4ffa6714de5d9dc249`  
		Last Modified: Wed, 06 May 2026 00:12:39 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90889b7f693a1edcd91ef3ad4a61ff7ae34496bf2c8b8c8d779783a099e1b4c6`  
		Last Modified: Wed, 06 May 2026 00:12:44 GMT  
		Size: 50.4 MB (50440549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9134453595996e1b8c2869f7a2f09bcbd0aadb594c1164061723d5a60d256fa2`  
		Last Modified: Wed, 06 May 2026 00:12:46 GMT  
		Size: 140.2 MB (140235938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8caf6bb56f855f253b6723ba3cc9bbcf5ea954a1a904f252364e03989e5b0ac0`  
		Last Modified: Wed, 06 May 2026 00:12:42 GMT  
		Size: 29.3 KB (29332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:b9c3fd59112ffcff770a353a9a14bf430720dc9acc5de08ead8c9d69ea17ac82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a69108aed7f7c8d851ecd60dd9f2c8ea2c6ddc5dc0eb994ef42d87341d2054`

```dockerfile
```

-	Layers:
	-	`sha256:1537fe2ad1cd20f605b465b7c0ef4f21498883257a6411a6fbf7571b90a11399`  
		Last Modified: Wed, 06 May 2026 00:12:43 GMT  
		Size: 5.4 MB (5419751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:906216ca6deb2cd41aab289fe415dbab1565a8541cca64ce04b0a19cf6f075c6`  
		Last Modified: Wed, 06 May 2026 00:12:42 GMT  
		Size: 23.3 KB (23345 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:b260d655a190f7e951d030a8b9aab2345db36c44a8e2ef84c455d475f57cd94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.4 MB (401400251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b617523a6671f10ca2c3e373f651034df5d81c0675db007246bbefce8b4a4797`
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
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 05 May 2026 23:52:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 05 May 2026 23:52:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 05 May 2026 23:52:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 05 May 2026 23:52:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 05 May 2026 23:52:36 GMT
CMD ["jshell"]
# Wed, 06 May 2026 00:18:51 GMT
CMD ["gradle"]
# Wed, 06 May 2026 00:18:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 May 2026 00:18:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 May 2026 00:18:51 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 May 2026 00:18:53 GMT
WORKDIR /home/gradle
# Wed, 06 May 2026 00:19:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 06 May 2026 00:19:16 GMT
ENV GRADLE_VERSION=9.5.0
# Wed, 06 May 2026 00:19:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Wed, 06 May 2026 00:19:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 May 2026 00:19:22 GMT
USER gradle
# Wed, 06 May 2026 00:19:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 06 May 2026 00:19:25 GMT
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
	-	`sha256:4a6f03167bd78052665789b8172f7a15f59a955ded2f9eb6d562b57e2a9d779d`  
		Last Modified: Tue, 05 May 2026 23:53:09 GMT  
		Size: 145.5 MB (145459990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64ee6ddf69356a3e4cd9aae22a18c8fa921d4faacfc1eebe7f9a6205ddbc4e1`  
		Last Modified: Tue, 05 May 2026 23:53:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6aadeeff9e6fcf3dbf533bed667e043e967774c8c7efcafbd1652033233e5dc`  
		Last Modified: Tue, 05 May 2026 23:53:06 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277443ee252e4d098765e3e44c435f609352ffa3cc594617946385b0f69bed87`  
		Last Modified: Wed, 06 May 2026 00:20:02 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef39a7216e3219373aebb1a49c3d749e048592f3ab7f57a8c254a8627877310f`  
		Last Modified: Wed, 06 May 2026 00:20:05 GMT  
		Size: 53.4 MB (53353695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e65344d995ae9bb983d7dc9447fbb180965a74a507fcc23477b6f11afbab56`  
		Last Modified: Wed, 06 May 2026 00:20:07 GMT  
		Size: 140.2 MB (140235947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34139c254d2713bb11852c53524c87e95961b6a980056be7742193b6289ff4ed`  
		Last Modified: Wed, 06 May 2026 00:20:02 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:cb439549e67404262b6a54647a5f05f1ba1d7caf02427b05dc96d22ca0672981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5440960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49a886e9477253eb3cf0b84a77d910c481de4023c013f54b1969e4a743f702e`

```dockerfile
```

-	Layers:
	-	`sha256:25b6e7301b7083be653c71df073a11fdfa715433a43921cd8f76163b4d7bbc3b`  
		Last Modified: Wed, 06 May 2026 00:20:03 GMT  
		Size: 5.4 MB (5417680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c64de2c075168f206db072cbc61c84b21eddcda335ca55654cb4f38381afac7`  
		Last Modified: Wed, 06 May 2026 00:20:02 GMT  
		Size: 23.3 KB (23280 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:3b6b800a7cae4a9a058e0f035814fff04e04d7e754485edad4cfc14a74df86c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380707345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae4c6ec0a0558211ce1c6ddd6b99fa8146ba0e648ad5b546e9ba65e60d0b12f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.openshift.expose-services=""
# Wed, 22 Apr 2026 05:05:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 22 Apr 2026 05:05:14 GMT
ENV container oci
# Wed, 22 Apr 2026 05:05:14 GMT
COPY dir:c10b61f0eaab474f87333058b5f0be076d9ca7550d40201126b259b146635cf0 in /      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 22 Apr 2026 05:05:15 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:94195acb2e6e678de51e9e05a9e10397a92e2f336a7de1f63b19aacc4230b754 in /usr/share/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:15 GMT
COPY file:94195acb2e6e678de51e9e05a9e10397a92e2f336a7de1f63b19aacc4230b754 in /root/buildinfo/labels.json      
# Wed, 22 Apr 2026 05:05:15 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "org.opencontainers.image.revision"="5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1" "build-date"="2026-04-22T05:05:02Z" "org.opencontainers.image.created"="2026-04-22T05:05:02Z" "release"="1776833838"org.opencontainers.image.revision=5bb1e5f6eb0dd42dce5d2f21f64a3a9feec995f1,org.opencontainers.image.created=2026-04-22T05:05:02Z
# Wed, 22 Apr 2026 18:16:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 18:16:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 18:16:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 22 Apr 2026 18:16:26 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 22 Apr 2026 18:16:26 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 22 Apr 2026 18:18:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 22 Apr 2026 18:18:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 22 Apr 2026 18:18:36 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 22 Apr 2026 18:18:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 22 Apr 2026 18:18:36 GMT
CMD ["jshell"]
# Tue, 28 Apr 2026 23:28:33 GMT
CMD ["gradle"]
# Tue, 28 Apr 2026 23:28:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 28 Apr 2026 23:28:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 28 Apr 2026 23:28:33 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 28 Apr 2026 23:28:33 GMT
WORKDIR /home/gradle
# Tue, 28 Apr 2026 23:28:38 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 28 Apr 2026 23:28:38 GMT
ENV GRADLE_VERSION=9.5.0
# Tue, 28 Apr 2026 23:28:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Tue, 28 Apr 2026 23:28:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 28 Apr 2026 23:28:42 GMT
USER gradle
# Tue, 28 Apr 2026 23:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 28 Apr 2026 23:28:43 GMT
USER root
```

-	Layers:
	-	`sha256:aac8159c3d9a48859bb2e3c581e3c2dc900b6a0665fa45fbd980e797d234b4a6`  
		Last Modified: Wed, 22 Apr 2026 06:11:17 GMT  
		Size: 38.1 MB (38131833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36bcbe215132f57438e633085ed9ba659acbb28bba079eaccc56fd117fd63d3`  
		Last Modified: Wed, 22 Apr 2026 18:17:46 GMT  
		Size: 30.4 MB (30386245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce43d2c8e46b1126687d6215a4402edd06ce64baf564b718e76616848868424`  
		Last Modified: Wed, 22 Apr 2026 18:20:02 GMT  
		Size: 135.6 MB (135629089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cee9f6be341ee932c7a427cd20aed368e54cfc7b21971a87af94c34cbcf1c3`  
		Last Modified: Wed, 22 Apr 2026 18:19:50 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca44688c2094c52874e1442eab6a60f4d53596b823fb1a534f15e751ac9defe2`  
		Last Modified: Wed, 22 Apr 2026 18:19:51 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c511d0e3d053f8020e7994d86f52efe16b2309b8481dd6d1a268a92b08ee065`  
		Last Modified: Tue, 28 Apr 2026 23:29:06 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b974d0ab675302413da99857c095eb791dc4a0b5eec0687e41d820e97fd0eae1`  
		Last Modified: Tue, 28 Apr 2026 23:29:07 GMT  
		Size: 36.3 MB (36319687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c24590b11a8b67ed93153267a81e43171b06c174a301fefdda8115e8076df2`  
		Last Modified: Tue, 28 Apr 2026 23:29:09 GMT  
		Size: 140.2 MB (140235945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae487672bff7b0e9f4c3b3d77bbde9b0d377dc074773ba2edf0a69b988fcc82`  
		Last Modified: Tue, 28 Apr 2026 23:29:06 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:21b7acf4581824d66e158b6961ea5f5ebda1d4b660996b231b8075d4a6818fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5427802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29742f77db1c9a02b74cc2c286c4e43163a150740b8648de0a5a7665f0203400`

```dockerfile
```

-	Layers:
	-	`sha256:021e80bd44ceeffdd52f657fb07d9f4c309c255758bdceaffe657bb0042e7d53`  
		Last Modified: Tue, 28 Apr 2026 23:29:06 GMT  
		Size: 5.4 MB (5404572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15e06f36e704dc54ea52485b138ca23cd0913ddabac748cd5386c1359882a3d9`  
		Last Modified: Tue, 28 Apr 2026 23:29:06 GMT  
		Size: 23.2 KB (23230 bytes)  
		MIME: application/vnd.in-toto+json
