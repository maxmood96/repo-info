## `gradle:8-jdk11-ubi9`

```console
$ docker pull gradle@sha256:49111ab6519ab2b6e74a38351874ebe43add951d6d571b2e04cf4ef979615aaa
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

### `gradle:8-jdk11-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:f8f3e6527a643cd098923da1edf6f6f91a1f8ec80fcdb651bec39f058dfa963d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.6 MB (387562761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922c30ae9d158a8f3c1699a4e3acb24d5a1cb1c24d86f07eccaee122a0e3a257`
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
# Tue, 12 May 2026 23:34:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:34:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:34:05 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:34:05 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 23:34:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:34:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:34:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:34:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:34:12 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:13:33 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:13:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:13:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:13:33 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:13:33 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:37 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:37 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 13 May 2026 00:13:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 13 May 2026 00:13:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:39 GMT
USER gradle
# Wed, 13 May 2026 00:13:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:13:40 GMT
USER root
```

-	Layers:
	-	`sha256:c06b8ad3393fea673394e067fccddfc7ef6d8cee753eba4c4dcd5d67792bfd4b`  
		Last Modified: Tue, 12 May 2026 06:00:36 GMT  
		Size: 40.0 MB (40022633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18273d0cc7c6f99e9c908aeafa44adfac56c239fe0137b4d6f62bfc5fad37926`  
		Last Modified: Tue, 12 May 2026 23:34:29 GMT  
		Size: 30.4 MB (30368048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964b8a7bbc601b11958b8273a8386df3dcbf0b9c956288a862476aa155c75265`  
		Last Modified: Tue, 12 May 2026 23:34:31 GMT  
		Size: 142.3 MB (142348809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d33dc72ed06cffa5aa1ddc8bd7124c1f9e97f65738a951411a36994a3f22eb`  
		Last Modified: Tue, 12 May 2026 23:34:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c77a9cb41ab90a334caeb01247390287f35379b5e24cf69b63bbd92dba4120`  
		Last Modified: Tue, 12 May 2026 23:34:27 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4022c3a46b0413507c4f91bc89a632d4e45f481ecb6f6fa5f637cd54d7156862`  
		Last Modified: Wed, 13 May 2026 00:13:57 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d6e09a15df68dca2b27d409126a4ad5539a922992dd4cdbac7a32dde3f3c26`  
		Last Modified: Wed, 13 May 2026 00:13:57 GMT  
		Size: 36.7 MB (36695668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ee78c6bb78afbd3678d996861c1b722d9947cd66835e728adc34f80b279a6d`  
		Last Modified: Wed, 13 May 2026 00:14:00 GMT  
		Size: 138.1 MB (138068534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac2e7ebfbcafab19eb7cde07d342e219cf97cdee5c38b0c0d5fa171ecd2defe`  
		Last Modified: Wed, 13 May 2026 00:13:56 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:79b6a1469725aaad3188407d11a2da1ef766b6e526cdc43ec7a1ef4eab3e49b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b262a459c1f8938e12d38419ee4536daee4fc17e1a000b9f3ba1d3520c6b412`

```dockerfile
```

-	Layers:
	-	`sha256:9e9799c9973de311ea3f24b9bb191953e216e140129e53e49a491bc329209aed`  
		Last Modified: Wed, 13 May 2026 00:13:56 GMT  
		Size: 5.4 MB (5424051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b898c643290e95abee91a56c93ab9af1295890564a2478d99c689415a12493f8`  
		Last Modified: Wed, 13 May 2026 00:13:55 GMT  
		Size: 24.5 KB (24453 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3a5bdf4880eadf9abde23cf967a4d1b98b4b17d91892b685c196484b8a137a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382191347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b248b2b770cd911f86379615c309c31a79310ed652da0896cc5dc92c363e2ea2`
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
# Tue, 12 May 2026 23:33:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:09 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 23:33:17 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:33:18 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:18 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:33:18 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:13:22 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:13:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:13:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:13:22 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:13:22 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:13:26 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:13:26 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 13 May 2026 00:13:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 13 May 2026 00:13:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:13:29 GMT
USER gradle
# Wed, 13 May 2026 00:13:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:13:29 GMT
USER root
```

-	Layers:
	-	`sha256:cd21d11a73b4a3fb6683533da05d561785e6bdfe61eb163870493206db32b8fc`  
		Last Modified: Tue, 12 May 2026 06:10:38 GMT  
		Size: 38.2 MB (38205025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c558d2effed4fc2841f4b28ea3f41643c0669d77c2ad98fb17de2bd2f2492e7`  
		Last Modified: Tue, 12 May 2026 23:33:35 GMT  
		Size: 30.8 MB (30788941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef3e7c3a40ab28b391b7a34f1cabba3e2c8f93edcdce049907e118ac65dad29`  
		Last Modified: Tue, 12 May 2026 23:33:39 GMT  
		Size: 139.0 MB (139040634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695e4da83ca8ad1bb012e85b800343f98019f21cdd6487ec384350ac289dfebe`  
		Last Modified: Tue, 12 May 2026 23:33:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1441f56dc39f2d713d6465a1330de93328429f1e4cf4467aa76883150048a0a1`  
		Last Modified: Tue, 12 May 2026 23:33:34 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa537769b45113bdab185050140bb56216cef17af1718de43134f16e20ed8d51`  
		Last Modified: Wed, 13 May 2026 00:13:46 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbfb333c118964866aff05647a41f20738f3e16e8550cb6ee1a469ab8df313d`  
		Last Modified: Wed, 13 May 2026 00:13:48 GMT  
		Size: 36.0 MB (36024522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c53a8a66e9e10cd13af4fe42897067f3a320ea6824f724910b7ecea71d250e`  
		Last Modified: Wed, 13 May 2026 00:13:50 GMT  
		Size: 138.1 MB (138068536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66f897d347ad2edee5e8c220336f2cbb2ff6a1854ae461174bc22954ce84081`  
		Last Modified: Wed, 13 May 2026 00:13:46 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:af71dc38fd94a30b8bb42fe1b36f52026aa5e75b0ae3e9225cbe1fda4982a2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db452fda75e24c5ca902d5e21100043cda4bb1e70e0bc90cff90c783a5181c14`

```dockerfile
```

-	Layers:
	-	`sha256:c46d22100a51363afb2c41e43fbec33a69835ec5afa5a46ab6afd4ad6e45639b`  
		Last Modified: Wed, 13 May 2026 00:13:46 GMT  
		Size: 5.4 MB (5424099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7ced63075155431f02fcdcb453ac3b288d295a8ce90ddf404771673f63d5eb`  
		Last Modified: Wed, 13 May 2026 00:13:46 GMT  
		Size: 24.6 KB (24650 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:d5136a8f04b76ac1ff7b22ba15c6502075a910177b65b846319a9e90d3e550ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382932460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60149f9435487fc466ff6853a0caf453cb2d132ace5dd66791057dfe635ac97`
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
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 23:33:46 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:33:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:50 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:33:50 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:16:23 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:16:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:16:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:16:23 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:16:23 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:16:34 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:16:34 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 13 May 2026 00:16:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 13 May 2026 00:16:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:16:38 GMT
USER gradle
# Wed, 13 May 2026 00:16:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:16:41 GMT
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
	-	`sha256:0800155cf197915ef8fde2a28c7d4170e2bab659c8b82a30a8e60c09dc74e16e`  
		Last Modified: Tue, 12 May 2026 23:34:24 GMT  
		Size: 129.6 MB (129614183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2300b6ce61f50693ee7771e41514404e07b976551933a45a8edac2889e28754b`  
		Last Modified: Tue, 12 May 2026 23:34:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4fc08cf1adfc69f26e663b5b9ac69379b35ab6a992aedb56dfc989fb159f6d`  
		Last Modified: Tue, 12 May 2026 23:34:21 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6e2b016b89508ab3a67f1fab74d449b00137ecd0a63ba1da72b1e7ec9fc729`  
		Last Modified: Wed, 13 May 2026 00:17:18 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7c203446f013183341d9e9833023d0d00bcc7821f783523c18fce07ed045d9`  
		Last Modified: Wed, 13 May 2026 00:17:20 GMT  
		Size: 37.9 MB (37931422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb92a26009bd3b729ec0cf8077958c2392739ef3c250dfa9d616034e2bc35e90`  
		Last Modified: Wed, 13 May 2026 00:17:23 GMT  
		Size: 138.1 MB (138068576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2596a04c70219a9575886800c3d44512d79701f1a8bc6388a1d7d6679e9fd25`  
		Last Modified: Wed, 13 May 2026 00:17:18 GMT  
		Size: 35.0 KB (35010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:4bf3ac97d87a552f07b58e045ab56b070704f9678a63b1c7ce62b4082969d53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd69472ead8da68645e125e3d991dbce0588373c77eb9c058827ecbc8bf69f68`

```dockerfile
```

-	Layers:
	-	`sha256:c2e3aeaca6d456597f037a5f9498bbd5c059adeca0cb9967bac1c19eb51bbba0`  
		Last Modified: Wed, 13 May 2026 00:17:18 GMT  
		Size: 5.4 MB (5420771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec010ac47413aa29c27781f6569a75a7ba43b240abf6174b396c1131bc5fe8d`  
		Last Modified: Wed, 13 May 2026 00:17:18 GMT  
		Size: 24.6 KB (24564 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:4767e0e8dfa7b7dde4968f4d71708576725bca01d81103d828636ba868b6ef6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.0 MB (366015240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f4c8c4ed4a4eca95fba62a6b99f7c22456683a93dcd1e0c26443fbb1cf1cac`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 12 May 2026 05:11:47 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 12 May 2026 05:11:47 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 12 May 2026 05:11:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 12 May 2026 05:11:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 12 May 2026 05:11:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 12 May 2026 05:11:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 12 May 2026 05:11:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:11:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 12 May 2026 05:11:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 12 May 2026 05:11:47 GMT
LABEL io.openshift.expose-services=""
# Tue, 12 May 2026 05:11:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 12 May 2026 05:11:47 GMT
ENV container oci
# Tue, 12 May 2026 05:11:48 GMT
COPY dir:249441911c8c0633ca798490aaa1299c161ab98598d4ab2b7470ccab434a7c48 in /      
# Tue, 12 May 2026 05:11:48 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 12 May 2026 05:11:48 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2026 05:11:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 12 May 2026 05:11:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 12 May 2026 05:11:48 GMT
COPY file:205d87f3ff6644c034e0dc9b6978b61083953f1a77745b1cda275d4a241fe854 in /usr/share/buildinfo/labels.json      
# Tue, 12 May 2026 05:11:48 GMT
COPY file:205d87f3ff6644c034e0dc9b6978b61083953f1a77745b1cda275d4a241fe854 in /root/buildinfo/labels.json      
# Tue, 12 May 2026 05:11:49 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="cbebc1cfad3d894eb79709424b198d17236aaba5" "org.opencontainers.image.revision"="cbebc1cfad3d894eb79709424b198d17236aaba5" "build-date"="2026-05-12T05:11:36Z" "org.opencontainers.image.created"="2026-05-12T05:11:36Z" "release"="1778562320"org.opencontainers.image.revision=cbebc1cfad3d894eb79709424b198d17236aaba5,org.opencontainers.image.created=2026-05-12T05:11:36Z
# Tue, 12 May 2026 23:33:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 23:33:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 23:33:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 23:33:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 23:33:23 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Tue, 12 May 2026 23:33:29 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 23:33:31 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 23:33:31 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 23:33:31 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 23:33:31 GMT
CMD ["jshell"]
# Wed, 13 May 2026 00:17:14 GMT
CMD ["gradle"]
# Wed, 13 May 2026 00:17:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 13 May 2026 00:17:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 13 May 2026 00:17:14 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 13 May 2026 00:17:15 GMT
WORKDIR /home/gradle
# Wed, 13 May 2026 00:17:39 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 13 May 2026 00:17:39 GMT
ENV GRADLE_VERSION=8.14.5
# Wed, 13 May 2026 00:17:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Wed, 13 May 2026 00:17:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 13 May 2026 00:17:46 GMT
USER gradle
# Wed, 13 May 2026 00:17:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 13 May 2026 00:17:48 GMT
USER root
```

-	Layers:
	-	`sha256:ce111e91e194b1445a42f490d2da50a425f89166a5a9cd92ae2933436bc449dc`  
		Last Modified: Tue, 12 May 2026 06:10:58 GMT  
		Size: 38.1 MB (38131193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2beef37fbe27a9395a329db26697bbffda5310b4cf235c92b7164ae6cd167e`  
		Last Modified: Tue, 12 May 2026 23:33:58 GMT  
		Size: 30.4 MB (30383170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed268b2ab2166f31002c001aafb87af0e58edd13c7ef6c098fd48ed5552497d`  
		Last Modified: Tue, 12 May 2026 23:34:00 GMT  
		Size: 123.1 MB (123061443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601144d8354d1054a69a06d1b4563a1fe82b6e4b4e4a99ae3bfad2b333a23d23`  
		Last Modified: Tue, 12 May 2026 23:33:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8c62a92f44f8fa74a4134bf52961ec80904ad3459a53fc0b77b78d2e2856b0`  
		Last Modified: Tue, 12 May 2026 23:33:50 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f04cb18a04a4c576a90fda92c7a1ee253c4ab7bb4d65cb7f75f25843e13be1`  
		Last Modified: Wed, 13 May 2026 00:18:39 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0399f02cf84650937b357bceb4eb79daa6a33694d18d6fad151174e56d5dd2bc`  
		Last Modified: Wed, 13 May 2026 00:18:43 GMT  
		Size: 36.3 MB (36331715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157e4281d981af169ecd2c2073a9bf4934d7a4cd7dbb322ba753f29aa8bd59c2`  
		Last Modified: Wed, 13 May 2026 00:18:46 GMT  
		Size: 138.1 MB (138068540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9f0cd6da05ab06c6e45b9257dff7ffa8c10ec9cfcaa126942f734503b4b59a`  
		Last Modified: Wed, 13 May 2026 00:18:39 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:ecdb4faa81ac6a67d0fbbfc9f289d701a3fb070dfc4d8cd794ebd22eaac9827b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5435150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877ce6d4e9120922e98f569e5a5cd8953d9990f6160633a5b760c977de1ed4ea`

```dockerfile
```

-	Layers:
	-	`sha256:30c027a5e8aa056413da7939b6c191cc00f9587fec6588f0f519abe4133c2804`  
		Last Modified: Wed, 13 May 2026 00:18:40 GMT  
		Size: 5.4 MB (5410660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881a1c0c3b3ba7a456ce8e324add8ab96fbd09b6184eff2b34c5f394f9d51c03`  
		Last Modified: Wed, 13 May 2026 00:18:39 GMT  
		Size: 24.5 KB (24490 bytes)  
		MIME: application/vnd.in-toto+json
