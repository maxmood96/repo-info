## `gradle:7-jdk8-ubi`

```console
$ docker pull gradle@sha256:7f9f692ce7af4693fce1bd6d582766c9d8dd0c2f6062cd48b596d6b09c95cdda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `gradle:7-jdk8-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:ca3de6aa6285981288a05e355795edcc9bfca2a00b85f16b8b7a3d3b5173558c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.2 MB (287248297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28673e160a1fe8e6d3da74622b4b37a8e806ce8c0dd0d6e612f466186aaa806`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL maintainer="Red Hat, Inc."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL vendor="Red Hat, Inc."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.openshift.expose-services=""
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sat, 05 Jul 2025 02:17:41 GMT
ENV container oci
# Sat, 05 Jul 2025 02:17:41 GMT
COPY dir:fed8131dab1a07775853004683d17f14115862719c3742630632a44de821b8a8 in / 
# Sat, 05 Jul 2025 02:17:41 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL "build-date"="2025-08-07T16:38:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER root
```

-	Layers:
	-	`sha256:7ceb420857b3cf642e9e34e4e12ebf8ca5ed092e6c4b4f69ce4ed011e9e8140a`  
		Last Modified: Thu, 07 Aug 2025 18:09:52 GMT  
		Size: 39.7 MB (39651301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b55bb71fee4a480bedb783398c1238429828f4678557a6323a353a0724a429`  
		Last Modified: Wed, 13 Aug 2025 23:01:57 GMT  
		Size: 27.5 MB (27538832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc5993f0fbfb2be05ef37341a83b42d0b3cf41bc9315a5f8e28dd65e78c16aa`  
		Last Modified: Wed, 13 Aug 2025 23:11:17 GMT  
		Size: 54.7 MB (54731895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad22b34f8d3109e076748151634a513495e118a8853fe2941423a41ba3bd2861`  
		Last Modified: Wed, 13 Aug 2025 23:01:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe4f027b093e502b20c744c0164fffe154feea3ca64191ee915a4d13f46aa03`  
		Last Modified: Wed, 13 Aug 2025 23:01:54 GMT  
		Size: 2.3 KB (2314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e87693ee0e08fe36bfc433c2c04adbec9f592d0ade2f90fb5d0d06d1cdaf62`  
		Last Modified: Wed, 13 Aug 2025 23:11:55 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50d2f6db7b90a2f66dbbfea932ba04494e5b3e56281cecd56a9c04cdc8e1f83`  
		Last Modified: Wed, 13 Aug 2025 23:12:07 GMT  
		Size: 36.8 MB (36797769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2412d1cab8521de35c67d82eab470b6cc943adc2378aa6e49c899e46c7a01d9c`  
		Last Modified: Thu, 14 Aug 2025 07:25:15 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f3762de5877314638f5c9c79b26b97521e24cdf1102ea2c4a26fbb5642ac5c`  
		Last Modified: Wed, 13 Aug 2025 23:11:56 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:af3be47268484793169e69074822c809a7ec486b83cb188787433af880458a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93dcaac3836e27c11b5b6a40ae37d65414f3cee71efdac1e726ec62381d1cc33`

```dockerfile
```

-	Layers:
	-	`sha256:0cff1a7a5bf792453750e0f8293d890d5d2653e84abc9bbb067aeedc2840d6b1`  
		Last Modified: Thu, 14 Aug 2025 02:19:18 GMT  
		Size: 5.4 MB (5420358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5832d287e2e35b5d444e7857ad55c3b5d516e0de0315216ffa0a1d38f6d5b6e8`  
		Last Modified: Thu, 14 Aug 2025 02:19:19 GMT  
		Size: 23.6 KB (23619 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8b6807c4cc9d05e691285bee1f4f15c800e8ac7bac6899ee48853a6efdadfbd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284420029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133a035ea0085ffe2afeb17df9af658172b8d7d0500d6723c3619b16ff75c961`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL maintainer="Red Hat, Inc."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL vendor="Red Hat, Inc."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.openshift.expose-services=""
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sat, 05 Jul 2025 02:17:41 GMT
ENV container oci
# Sat, 05 Jul 2025 02:17:41 GMT
COPY dir:5da5b397cee17643fbcc12434bebce628a4ff854389d189d0166a1ebc5e815db in / 
# Sat, 05 Jul 2025 02:17:41 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL "build-date"="2025-08-07T16:43:31" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
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
		Last Modified: Thu, 14 Aug 2025 17:24:27 GMT  
		Size: 36.2 MB (36248957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8835a0db3d14f19c0687e8d8bedb420b54925010d31a850cb7429805ca9a60f1`  
		Last Modified: Thu, 14 Aug 2025 17:24:30 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbde8e928aae91e7de99a6d8c32f7cc6af4841c7b847c672c1b964010d394753`  
		Last Modified: Thu, 14 Aug 2025 17:32:59 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:5519cd7948ca3c7f48b48c1bf76699f9ca749555b61fafc142025226e1962c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5444244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e456ec4527b93811bff6e188a73b09e0edcddf20f3c19b797c3a3f8935c41dd4`

```dockerfile
```

-	Layers:
	-	`sha256:0e3959dd31b369f542de6189891e3e0b53f9925ce40cf79efcdfc194ae199914`  
		Last Modified: Thu, 14 Aug 2025 20:19:25 GMT  
		Size: 5.4 MB (5420468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:380db1763c26c5c55be39b07bc0ee2668d8cf52d84735e77d87584c4063e3fe3`  
		Last Modified: Thu, 14 Aug 2025 20:19:26 GMT  
		Size: 23.8 KB (23776 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:22e7eb4945305e3678462f7a19728362b1f64cd38e1c0621f11c9db0e0b2e503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292832514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fc2b0dbbb5ed67f2b4a7c312eeae787076fbc83ecb8dd007cf51055ac46ccb`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL maintainer="Red Hat, Inc."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL vendor="Red Hat, Inc."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.openshift.expose-services=""
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL io.openshift.tags="minimal rhel9"
# Sat, 05 Jul 2025 02:17:41 GMT
ENV container oci
# Sat, 05 Jul 2025 02:17:41 GMT
COPY dir:b1e34ea7a28362356126333145a3caa4ced0141e04688d16b04ab649c669f43c in / 
# Sat, 05 Jul 2025 02:17:41 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 02:17:41 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Sat, 05 Jul 2025 02:17:41 GMT
LABEL "build-date"="2025-08-07T16:44:50" "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="14d0d41651f155541d4ccbcf34f4f03159bc36b2" "release"="1754584681"
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Jul 2025 02:17:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 02:17:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='19552c1cf7f5c18290a6bdcd6757f70ea5c331a2bc0dd7a3b3120e8dbc4b4891';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u462b08.tar.gz';          ;;        ppc64le)          ESUM='3e4dbc94ebd299b60d8168b1d33cdae1f619db9403aaefd65d0b643615d596cc';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u462b08.tar.gz';          ;;        x86_64)          ESUM='5d64ae542b59a962b3caadadd346f4b1c3010879a28bb02d928326993de16e79';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u462b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip; # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 05 Jul 2025 02:17:41 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:17:41 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:17:41 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
ENV GRADLE_VERSION=7.6.6
# Sat, 05 Jul 2025 02:17:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
USER gradle
# Sat, 05 Jul 2025 02:17:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 05 Jul 2025 02:17:41 GMT
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
	-	`sha256:f117be260b623e928a0400dfac00b6733aff1d554ad1d59186c47c1d2dba94cc`  
		Last Modified: Thu, 14 Aug 2025 04:46:25 GMT  
		Size: 52.2 MB (52165986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1530f420948030f5736e2bd39db0ab2c22e7123c7b40a215fafce725d25bb286`  
		Last Modified: Thu, 14 Aug 2025 04:46:30 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f721d5fcc43b94d4b73c68ad2888e24e69dfedaeb88832e27f719780063154c8`  
		Last Modified: Thu, 14 Aug 2025 04:46:30 GMT  
		Size: 2.3 KB (2316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff6958d8949bca0ad2570d34151d13a1fb338bdd03d5c141858a3a18c13c37d`  
		Last Modified: Thu, 14 Aug 2025 12:25:28 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2cbdea6eaa8aa5ff29c0e24d650e85d2c2fa67f2670f0ed634145aaa93af9c`  
		Last Modified: Thu, 14 Aug 2025 12:13:22 GMT  
		Size: 38.1 MB (38121788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8fcffcfc4d9db5c0b6350bec8b804431fc39a761bae7a3aaff164f28377b45`  
		Last Modified: Thu, 14 Aug 2025 12:18:05 GMT  
		Size: 128.5 MB (128469422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f18283467a1c51b8953a38facf8877e8a1fcb3754d4666d11e767a5881b733`  
		Last Modified: Thu, 14 Aug 2025 12:18:36 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:aea64a2ddc63be0e6c14d31e4af60ad9f2bbd3c13bc3f4746afd9da3b12e6482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3033a0009b77204eb80f441e2e5e404f776c7ef87458bdc561352e40fc58bbbe`

```dockerfile
```

-	Layers:
	-	`sha256:007948f359b05d085ca7adcc205429e1662020f75ef4ee24c81631c075c96f5e`  
		Last Modified: Thu, 14 Aug 2025 14:19:02 GMT  
		Size: 5.4 MB (5418276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b586ce2bf55a4dc5f93fe50b74addc0e3783cca7aa1a6cd77cf5571f4be9d68`  
		Last Modified: Thu, 14 Aug 2025 14:19:02 GMT  
		Size: 23.7 KB (23681 bytes)  
		MIME: application/vnd.in-toto+json
