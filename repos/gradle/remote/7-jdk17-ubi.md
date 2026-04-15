## `gradle:7-jdk17-ubi`

```console
$ docker pull gradle@sha256:d8fe924423f75c8c3aed73a13d953d77b82315f083542d9c2f5d65f7d1c62bad
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

### `gradle:7-jdk17-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:a00ed123e37153adda6ed8dda3cbc699f4cf23a8a1cacff522b12a784db26258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.2 MB (381246214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aac138ee39bad447f5e6073fa9a1f0600e94c0af632ed22278de6339f8a7dd8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:26:37 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:26:37 GMT
ENV container oci
# Mon, 13 Apr 2026 18:26:38 GMT
COPY dir:5191e1ce97881b91cd281225b61de5b907dbc286c69b6681e228608a9d6bab0b in /      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:26:38 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:38 GMT
COPY file:22a393f43688b6747c863a4550da665d92705a5e9519cc2d1c97b9f7499127bb in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:26:39 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:26:26Z" "org.opencontainers.image.created"="2026-04-13T18:26:26Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:26:26Z
# Tue, 14 Apr 2026 20:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:45:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:45:53 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:45:53 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 14 Apr 2026 20:46:00 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:46:01 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:46:01 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:46:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:46:01 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:57:58 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:57:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:57:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:57:58 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:57:59 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:59:49 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:59:49 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:59:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 20:59:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:59:52 GMT
USER gradle
# Tue, 14 Apr 2026 20:59:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:59:52 GMT
USER root
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314b7d27c846553831a43b2d28b9d4110c589c2661a4b11d8ea4fd173571ebae`  
		Last Modified: Tue, 14 Apr 2026 20:46:19 GMT  
		Size: 30.4 MB (30369723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006b0259eb5bfe09c7e9737746b0a7f6f6d2b5bb6cf05af621aea39665a3567c`  
		Last Modified: Tue, 14 Apr 2026 20:46:21 GMT  
		Size: 145.6 MB (145637114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19148ffffd37817fc1192ba8264e10a9b0343a761524e2a1089f1fc36827363f`  
		Last Modified: Tue, 14 Apr 2026 20:46:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e8c570d902b1e8dbe7f79b97fc7bf7efb3d60de485aff5f892e1e55d90a8f6`  
		Last Modified: Tue, 14 Apr 2026 20:46:17 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b843649eb0d8a555a113199380ab9746070a49fd6af1aba463f7bc766736f92`  
		Last Modified: Tue, 14 Apr 2026 20:58:21 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23cf27ec9288acac90bdc524dc01e114f5ebbea7d5dac13f3cdfb7bad434dea2`  
		Last Modified: Tue, 14 Apr 2026 21:00:15 GMT  
		Size: 36.7 MB (36694341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec76350994a63195482a4fe71ac67a96ee3eeb269b9c89fccc953ebc551c1417`  
		Last Modified: Tue, 14 Apr 2026 21:00:17 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebca1cff85747c78b14b55106e0691495097716d8718638aa823c2c3b75323b`  
		Last Modified: Tue, 14 Apr 2026 21:00:15 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:7f2411340ddd786910020a4a01bc373997ef5fa382ab76d25e6402535fab212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5338140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd58bb31ebf570dadb4d549c8bfc1ed51d1b9b4887a623c24c042ed73aefd86d`

```dockerfile
```

-	Layers:
	-	`sha256:fdf3e1c03c92499b958304b14d7c964fab4967ad0b5c5530a6ec2348adb10cf6`  
		Last Modified: Tue, 14 Apr 2026 21:00:09 GMT  
		Size: 5.3 MB (5314562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2013ce9084fc13d1ebb2c50217b6a1b600eabef5d59b8bdc65d4138a26bade7a`  
		Last Modified: Tue, 14 Apr 2026 21:00:08 GMT  
		Size: 23.6 KB (23578 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1999222ac3eae2ab91efa8efe610b50ee250d2b7bef4c9de56f372dd4d179d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.0 MB (378003043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd5cd66ca1b02ae297ce7c16028d32d93cd4d6033d9f752bbd7ff739bebcf27`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:28:23 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:28:23 GMT
ENV container oci
# Mon, 13 Apr 2026 18:28:24 GMT
COPY dir:50ceff14380ca413ec2568b248e47effdceffdd30707fc734a4741e902f97450 in /      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:28:24 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
COPY file:20aaf8ce1e0136dca2eb48dbc70df34738ee917c73847beed0478c7b853d8231 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:28:24 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:28:10Z" "org.opencontainers.image.created"="2026-04-13T18:28:10Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:28:10Z
# Tue, 14 Apr 2026 20:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:45:39 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:45:39 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 14 Apr 2026 20:45:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:48 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:55:29 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:55:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:55:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:55:29 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:55:29 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:56:10 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:56:10 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:56:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 20:56:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:56:13 GMT
USER gradle
# Tue, 14 Apr 2026 20:56:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:56:13 GMT
USER root
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4332255aeff932adaf7628e6cb6c0364c883067ddba5dd66b327aeca31c8dd1d`  
		Last Modified: Tue, 14 Apr 2026 20:46:06 GMT  
		Size: 30.8 MB (30797447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdff3714a39131ecb91ba7cf59ecaedc8ce2cc63afced92991a93eb20619dbe1`  
		Last Modified: Tue, 14 Apr 2026 20:46:08 GMT  
		Size: 144.4 MB (144446594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce0c90f1649d7f9483a6e45d69c3b895dcabba29069eb8e553be9033ca745fb`  
		Last Modified: Tue, 14 Apr 2026 20:46:05 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b1395b3f5d0700230f5d1c1b72d767eddc8b684a5e8a00a2607e8f5caf71d`  
		Last Modified: Tue, 14 Apr 2026 20:45:54 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6971fc6fe094df7b970119c53124f583f4ee766f229e6e83b1968d2c6922f4`  
		Last Modified: Tue, 14 Apr 2026 20:55:54 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6eaf8bbc75251eeb27dba787f44cc6a594714fff8dd92f9229127d56426ea6a`  
		Last Modified: Tue, 14 Apr 2026 20:56:29 GMT  
		Size: 36.0 MB (36025798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef49357d9e35494c6c10b6d76916fea1f108e437299c7868a896ed5cb6cf201b`  
		Last Modified: Tue, 14 Apr 2026 20:56:31 GMT  
		Size: 128.5 MB (128469418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bccc1617b7308a9576a26b13ae90ff56acc63a2ca9b739d8def470154157404`  
		Last Modified: Tue, 14 Apr 2026 20:56:28 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:be6debfe6c1cc52cfaa33931b242649d7129cfa62aa3177f7ae8f2dbebf01108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e29e7d5cebe7b1db334dd9fce95e70b7de03587782656c7d28ba363a4fd832`

```dockerfile
```

-	Layers:
	-	`sha256:d510cf65711e74dfeab99bb1bde71522d6a84712f79825c688ce09f3fe9b9101`  
		Last Modified: Tue, 14 Apr 2026 20:56:28 GMT  
		Size: 5.3 MB (5313972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c233987efd397072766bbb5d5644cd2bd340b5ee49d84bf19172d2c94f8777`  
		Last Modified: Tue, 14 Apr 2026 20:56:28 GMT  
		Size: 23.8 KB (23752 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:10991275f6520b64f2f8e17f1622bf1a0df2b1e50e66179618e868d7e2f1503e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389192821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab90db6961437f283c4243e6485e139bfef5d4482b77455b5d82cedae2e41c7`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:29:33 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:29:33 GMT
ENV container oci
# Mon, 13 Apr 2026 18:29:34 GMT
COPY dir:24fb0b263f289ef569c594958817053360bec0e0bfe2720b67eb4bf6d63e4515 in /      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:29:34 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:7062c8f1fa2df3b89f0d90bf3890fde04fbbd54d614aefabecd07515e8bba176 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:29:34 GMT
COPY file:7062c8f1fa2df3b89f0d90bf3890fde04fbbd54d614aefabecd07515e8bba176 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:29:35 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:29:23Z" "org.opencontainers.image.created"="2026-04-13T18:29:23Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:29:23Z
# Tue, 14 Apr 2026 20:44:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:44:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:44:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:44:11 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 14 Apr 2026 20:45:49 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:52 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:52 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:52 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:55:02 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:55:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:55:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:55:02 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:55:03 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:56:42 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:56:42 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:56:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 20:59:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:59:41 GMT
USER gradle
# Tue, 14 Apr 2026 20:59:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:59:43 GMT
USER root
```

-	Layers:
	-	`sha256:a8de600aa1d03790e68a950fc8a9160a10a53282e2415c939e6f6e1b5180c553`  
		Last Modified: Tue, 14 Apr 2026 00:13:55 GMT  
		Size: 44.4 MB (44444159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eea7503b93e046e3992230236cc9f313ea26fd31522ce2a84d764d8f98a753d`  
		Last Modified: Tue, 14 Apr 2026 20:44:47 GMT  
		Size: 32.8 MB (32849099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92141be9020b830faabeb5d42f13aa811e9e55b91ee07dc19c5703fdf158382`  
		Last Modified: Tue, 14 Apr 2026 20:46:36 GMT  
		Size: 145.5 MB (145460044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6c8251aa5aa0d277d2f6c2fd4d045f852688071ea6014bac2d14713b06ee2b`  
		Last Modified: Tue, 14 Apr 2026 20:46:32 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48b18d09380b18e4f8b61ca15999205659e9ff682fecdda8e227862db5c39b8`  
		Last Modified: Tue, 14 Apr 2026 20:46:32 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc64d920e5b636e66a7d24ceb308ff641aaa8c41e82a2e783d452782056cdfe`  
		Last Modified: Tue, 14 Apr 2026 20:56:13 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7d6a540c5e2df17280ff68b638afa3018e674934340fe13811e19827ece898`  
		Last Modified: Tue, 14 Apr 2026 20:57:25 GMT  
		Size: 37.9 MB (37930920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b55a672a2e9a6a4fa0a7045d44f98d580721993e8c1ec6cc31251f0ced4324`  
		Last Modified: Tue, 14 Apr 2026 21:00:26 GMT  
		Size: 128.5 MB (128469426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7bdfc5cebf066d39ba15b067919d696e9175820a9b3b2a3398231702726177`  
		Last Modified: Tue, 14 Apr 2026 21:00:22 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:f7fbc573162336e7b0f2d53a8dcd9603013c9e107047a73f6c5ae85dde1d1a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aab16f2a72c8bb3fed4ff75755aea1315ce5bd702732f91b2a423e5f3c4853a`

```dockerfile
```

-	Layers:
	-	`sha256:afe89ed873795c3aa0d0a5979b89b340221f34cf1eb6d31a3419cc97b5de7b39`  
		Last Modified: Tue, 14 Apr 2026 21:00:23 GMT  
		Size: 5.3 MB (5311889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3a4b7ac1b292c515c786921b585224a2e3ed2ce5fac6a0faa06d5f043a89bf0`  
		Last Modified: Tue, 14 Apr 2026 21:00:22 GMT  
		Size: 23.6 KB (23641 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:1af5a1bdd0b5b4481f2e66471a786e81aefd14d2d9f122df3ac3e36ad09d1a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368972825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097029e319b89c4e6cd5c5ed72f65b8f3db45ac7089d1863fa6b0ac6e4978de0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL io.openshift.expose-services=""
# Mon, 13 Apr 2026 18:35:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 13 Apr 2026 18:35:03 GMT
ENV container oci
# Mon, 13 Apr 2026 18:35:04 GMT
COPY dir:aad81c97bb1c65f7a47ee3ef6c9d703278e603b565bbb15c18d20e040058016c in /      
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 13 Apr 2026 18:35:04 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:936893ec4ec7da36a797e7c4e078694c2e39d7f412ff09f777a9236ebad6a5e4 in /usr/share/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:35:04 GMT
COPY file:936893ec4ec7da36a797e7c4e078694c2e39d7f412ff09f777a9236ebad6a5e4 in /root/buildinfo/labels.json      
# Mon, 13 Apr 2026 18:35:04 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "org.opencontainers.image.revision"="49cc6237764cacc4684bc968dd9fc53fb8abd12c" "build-date"="2026-04-13T18:34:52Z" "org.opencontainers.image.created"="2026-04-13T18:34:52Z" "release"="1776104705"org.opencontainers.image.revision=49cc6237764cacc4684bc968dd9fc53fb8abd12c,org.opencontainers.image.created=2026-04-13T18:34:52Z
# Tue, 14 Apr 2026 20:44:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:44:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:44:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:44:14 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:44:14 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 14 Apr 2026 20:44:20 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:44:22 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:44:22 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:44:22 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:44:22 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:55:11 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:55:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:55:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:55:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:55:11 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:56:21 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:56:21 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 14 Apr 2026 20:56:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 14 Apr 2026 20:56:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:56:25 GMT
USER gradle
# Tue, 14 Apr 2026 20:56:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:56:26 GMT
USER root
```

-	Layers:
	-	`sha256:188bc35e04514e4f35552e12dec8be6787ac365d49a3ea7fa542d4acf61bfd45`  
		Last Modified: Tue, 14 Apr 2026 00:13:48 GMT  
		Size: 38.1 MB (38114710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d5e9aa58e94c2dbfeaff290529d0e84d07cfc694fd4bed706be1ade8b27765`  
		Last Modified: Tue, 14 Apr 2026 20:44:39 GMT  
		Size: 30.4 MB (30388919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3694c04c2b0e103830304f1bb8a2cd52273d85e1a9b9e91f18993f7da01daed7`  
		Last Modified: Tue, 14 Apr 2026 20:44:50 GMT  
		Size: 135.6 MB (135629129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f8062647d70f2df4bc67e1f03e17757a137387f4f304b432698d9e2df59a6e`  
		Last Modified: Tue, 14 Apr 2026 20:44:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6571b33cd30d837c41592b22f7c7ab835d3953355c28cf3f3489fddd06c1acce`  
		Last Modified: Tue, 14 Apr 2026 20:44:47 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfdae500121b3343dc47425900d03187d3a02b27d832744bb1f19d8a8935bbd`  
		Last Modified: Tue, 14 Apr 2026 20:55:49 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5eda4af630899887d33e3412004575463108c694f7263a32a7de4abf093fd8d`  
		Last Modified: Tue, 14 Apr 2026 20:56:52 GMT  
		Size: 36.3 MB (36331481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5141edebacfa258d6948e7d5e41a56bb9cd57899421db7d307963bd38a61ee91`  
		Last Modified: Tue, 14 Apr 2026 20:56:54 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d54416fa7793b561a2e7319ff08520335b875733b0069496eb33cf7b700add`  
		Last Modified: Tue, 14 Apr 2026 20:56:51 GMT  
		Size: 35.0 KB (35004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:53db12fbc2daa711ae12e4f5905512b5549d3197c28586c49fbb8ebb8f0d7acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5324746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1593c4139dc53e169fc92f83c4f4442aba364e72f328c7433c911c98b11b4fdd`

```dockerfile
```

-	Layers:
	-	`sha256:124dae374cfab2c02b02d43e44a373f71d10babfdd1df2e1c5bdbbf23a4c785e`  
		Last Modified: Tue, 14 Apr 2026 20:56:51 GMT  
		Size: 5.3 MB (5301167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb5084287c8a4324145c69b29ed9072bf30b8199c654c058d66b1a00510004d5`  
		Last Modified: Tue, 14 Apr 2026 20:56:51 GMT  
		Size: 23.6 KB (23579 bytes)  
		MIME: application/vnd.in-toto+json
