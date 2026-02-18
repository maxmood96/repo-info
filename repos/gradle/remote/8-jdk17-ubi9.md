## `gradle:8-jdk17-ubi9`

```console
$ docker pull gradle@sha256:830afe090d3aadc57f264e80f0289bf05f0e92c10a2578a5728e8d1ebfec84ad
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

### `gradle:8-jdk17-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:ecb26dd97eef1098023fcebb8003939b4a3564cc0a2a9c1a65f643831e130325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 MB (390221890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b3b320c0f7882fd55262f96bda48d8f7372826b0c6dc08ee83c30266b5638`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:42:45 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:42:45 GMT
ENV container oci
# Tue, 17 Feb 2026 16:42:46 GMT
COPY dir:a84da6f36b88f4eb0d6c411f65b34c1a9d85150d3035dd516db4ece0c2569465 in /      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:42:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
COPY file:6326b4becf4dcc53eab9a0e80efe304ada5421165d0586862d969cb5fa826bd8 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:42:46 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:42:34Z" "org.opencontainers.image.created"="2026-02-17T16:42:34Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:42:34Z
# Wed, 18 Feb 2026 19:20:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:20:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:20:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:20:13 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:20:13 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 18 Feb 2026 19:20:20 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Feb 2026 19:20:21 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:20:21 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:20:21 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 19:20:21 GMT
CMD ["jshell"]
# Wed, 18 Feb 2026 20:10:49 GMT
CMD ["gradle"]
# Wed, 18 Feb 2026 20:10:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 18 Feb 2026 20:10:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 18 Feb 2026 20:10:49 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 18 Feb 2026 20:10:49 GMT
WORKDIR /home/gradle
# Wed, 18 Feb 2026 20:10:54 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 18 Feb 2026 20:10:54 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 18 Feb 2026 20:10:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 18 Feb 2026 20:10:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 18 Feb 2026 20:10:56 GMT
USER gradle
# Wed, 18 Feb 2026 20:10:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 18 Feb 2026 20:10:57 GMT
USER root
```

-	Layers:
	-	`sha256:4638e3415987f378f2d6dd70f9c6a2869dd5ebd09e3510ba45e46bbb6ec1a3dd`  
		Last Modified: Tue, 17 Feb 2026 18:08:54 GMT  
		Size: 40.0 MB (40033596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d60ee8dda47348ba7c3b9448836c23feb66fbd93dbb5f746a04ebbfa5c6d0d`  
		Last Modified: Wed, 18 Feb 2026 19:20:37 GMT  
		Size: 30.4 MB (30395363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f00d78211bd267e672a5f4b436ee95fa2d4d0c3c57c4b204af69a72e4601a`  
		Last Modified: Wed, 18 Feb 2026 19:20:40 GMT  
		Size: 145.6 MB (145637112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356fae2dd665ab4cc483096387f27fe65774536e12fdec711178078cce739b0d`  
		Last Modified: Wed, 18 Feb 2026 19:20:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585004369156eed8b294da0c1ff4120c14f5977f2e191c4da3d8d2644b03e2c6`  
		Last Modified: Wed, 18 Feb 2026 19:20:36 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89095b776daa3cf97f67cead9d6dfc5f472e41169dcebe531665c5fcba51ffdb`  
		Last Modified: Wed, 18 Feb 2026 20:11:14 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df183fdf1f08c543956c1c8a607fde1e90f1a4cb6062a6ba01c037ee5b53dbe1`  
		Last Modified: Wed, 18 Feb 2026 20:11:16 GMT  
		Size: 36.7 MB (36708491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091434549aaec1ec4868d03c6ff4d13235f026e61085264a9c59b12076726653`  
		Last Modified: Wed, 18 Feb 2026 20:11:18 GMT  
		Size: 137.4 MB (137388272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1729412553b30c94125a7ae2c10d065bec3365f368a8867aa5ecc0192c088e9b`  
		Last Modified: Wed, 18 Feb 2026 20:11:14 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:8a4462d67758b5864be2fd69cdf2f65d03a4716473e003ad1e9213499866ca32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5427458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b4a0ab84fb946df2d711a99f28c91a0ac7fe1562f53ebb268e12b46e5f8880c`

```dockerfile
```

-	Layers:
	-	`sha256:57498bd8731e64320e16865b301a12664c93e62a0f0fced7e526416c15f74a15`  
		Last Modified: Wed, 18 Feb 2026 20:11:14 GMT  
		Size: 5.4 MB (5403905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa4a33b1e774d172494de9cc7a59c227467e251a90e1ae0989287e39f349fca`  
		Last Modified: Wed, 18 Feb 2026 20:11:14 GMT  
		Size: 23.6 KB (23553 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fe171558b3935bd49a310195c17fcd77100020f05b5a82dd3667e30c26f663d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (386984462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6f48fdb3dbc3a984ccbe9ebcc4f05869e020100e8b81057c07c0a134d140ce`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 16:45:44 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 16:45:44 GMT
ENV container oci
# Tue, 17 Feb 2026 16:45:45 GMT
COPY dir:ac0ab1292a52ccb276077ed994531e1a3deef7d271c3502d95032264a0448d19 in /      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 16:45:45 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:45 GMT
COPY file:b6e9611fd18f4ab100ec73ea6037b1118108a414096af83dfb78d47ad0a2b249 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 16:45:46 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T16:45:31Z" "org.opencontainers.image.created"="2026-02-17T16:45:31Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T16:45:31Z
# Wed, 18 Feb 2026 19:19:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:19:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:19:00 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:19:00 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 18 Feb 2026 19:19:07 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Feb 2026 19:19:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:19:09 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:19:09 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 19:19:09 GMT
CMD ["jshell"]
# Wed, 18 Feb 2026 20:10:35 GMT
CMD ["gradle"]
# Wed, 18 Feb 2026 20:10:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 18 Feb 2026 20:10:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 18 Feb 2026 20:10:35 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 18 Feb 2026 20:10:35 GMT
WORKDIR /home/gradle
# Wed, 18 Feb 2026 20:10:39 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 18 Feb 2026 20:10:39 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 18 Feb 2026 20:10:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 18 Feb 2026 20:10:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 18 Feb 2026 20:10:42 GMT
USER gradle
# Wed, 18 Feb 2026 20:10:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 18 Feb 2026 20:10:43 GMT
USER root
```

-	Layers:
	-	`sha256:063fbd5fac6af91f4042bbe66bae69795aa46675d5b0c800ed195ad79ed8fb02`  
		Last Modified: Tue, 17 Feb 2026 18:09:11 GMT  
		Size: 38.2 MB (38202534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6e3f6623de46368404c3b3f7eb8471e6f3898a185863e09a3e1fe336fb831e`  
		Last Modified: Wed, 18 Feb 2026 19:19:28 GMT  
		Size: 30.8 MB (30825793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73dd1a7ab76865f5d33b7bfe0b63525b397f536b998d4094d18e7bf38604cad`  
		Last Modified: Wed, 18 Feb 2026 19:19:30 GMT  
		Size: 144.4 MB (144446524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289debeed214d85e415ecf131c512f9544b831a9f366f3d3c4fc04fefcfbdb1f`  
		Last Modified: Wed, 18 Feb 2026 19:19:26 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60f121722920d72cdfe795b23fb944081c541982713b90b5d7864fd84e4b4cc`  
		Last Modified: Wed, 18 Feb 2026 19:19:27 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f2badf943e0505bf386d6342daa4d32ebbbee41ff4680bfde5a5a3cc4d31b8`  
		Last Modified: Wed, 18 Feb 2026 20:11:00 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825c7e6f68173cb0eaf6d8f2d92ee090292479f477ef60f54f0e3ae40d1239d0`  
		Last Modified: Wed, 18 Feb 2026 20:11:01 GMT  
		Size: 36.1 MB (36057644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee00ad7bb6a9690eeb99795a34557cfbf9fdb912bb936776d823d3040d01b6f`  
		Last Modified: Wed, 18 Feb 2026 20:11:04 GMT  
		Size: 137.4 MB (137388277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5da4ec6042eb2ae32b04a40e30ae878c5eb77b2d84e523b34163150501021e`  
		Last Modified: Wed, 18 Feb 2026 20:11:00 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:01cd1557b0bd9d72f886f8124d7444e571dcfd4a76e6a1d550e4b36e3b78c192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5427037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031b1fba2ce150c7ea47543fc132b837ffebabf60f8e5f4d7fc146541e3eac31`

```dockerfile
```

-	Layers:
	-	`sha256:e2a5521c56f1510986d8b510949c0b8382befbc81f569784ebca40420676bd53`  
		Last Modified: Wed, 18 Feb 2026 20:11:00 GMT  
		Size: 5.4 MB (5403311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892d518d57fac5b87a5867f8c3779da09506dfdc10ee2a3b44caf03931cc7798`  
		Last Modified: Wed, 18 Feb 2026 20:10:59 GMT  
		Size: 23.7 KB (23726 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:07488587193c8c4db9742940d2786ec5ba5d22703cf8a709b3fb7bde33fdf252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.2 MB (398162809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa6fc66c50da8bc4a1dd35e0652a2ad6a97687bf1e42241a41c03ea5807062a`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 17:14:47 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 17:14:47 GMT
ENV container oci
# Tue, 17 Feb 2026 17:14:48 GMT
COPY dir:3a75322911f167c45a527d249b8b7a1bb61960bd0414c69e2c48ff05f3aaaa64 in /      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 17:14:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:4d5fe83a4c701a100e1eaed18157926865f67ffe30ea0c801e48164ab289c12d in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:14:48 GMT
COPY file:4d5fe83a4c701a100e1eaed18157926865f67ffe30ea0c801e48164ab289c12d in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:14:48 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T17:14:36Z" "org.opencontainers.image.created"="2026-02-17T17:14:36Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T17:14:36Z
# Wed, 18 Feb 2026 19:22:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:22:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:22:09 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:22:09 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 18 Feb 2026 19:24:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Feb 2026 19:24:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:24:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:24:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 19:24:12 GMT
CMD ["jshell"]
# Wed, 18 Feb 2026 20:09:18 GMT
CMD ["gradle"]
# Wed, 18 Feb 2026 20:09:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 18 Feb 2026 20:09:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 18 Feb 2026 20:09:18 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 18 Feb 2026 20:09:19 GMT
WORKDIR /home/gradle
# Wed, 18 Feb 2026 20:11:14 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 18 Feb 2026 20:11:14 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 18 Feb 2026 20:11:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 18 Feb 2026 20:11:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 18 Feb 2026 20:11:21 GMT
USER gradle
# Wed, 18 Feb 2026 20:11:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 18 Feb 2026 20:11:23 GMT
USER root
```

-	Layers:
	-	`sha256:722693878ac364b9d2ee6aa4d50e67ce459b9548beed24d0bb6ff115844b6e5d`  
		Last Modified: Tue, 17 Feb 2026 18:09:24 GMT  
		Size: 44.5 MB (44450261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bee69fcb88d423dd51b4ae1e9aa4be9eb53f1df38695a23566fd8e316cd932`  
		Last Modified: Wed, 18 Feb 2026 19:22:54 GMT  
		Size: 32.9 MB (32872323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b363e4f38076cbd4211aba85a759fc2ad932ce3d683eee66f6cc25b867b1f7b1`  
		Last Modified: Wed, 18 Feb 2026 19:25:07 GMT  
		Size: 145.5 MB (145460003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e33330617d56daaeeff0816e4939090c45d787d894755756d48c9e7793478d`  
		Last Modified: Wed, 18 Feb 2026 19:25:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a3d2c7ada4fea6a3e87e1211d2e9e38d781c5fa8c0712edf8453a1f1a7ee95`  
		Last Modified: Wed, 18 Feb 2026 19:25:04 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af410625489aa6f039fca5258cbb9a6f64abeaf963d8b8b261b270b5a6246de9`  
		Last Modified: Wed, 18 Feb 2026 20:10:35 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf4b7a19040a872759e3176aeeea74f1522aedcfed4aa549a0381c9a3574e87`  
		Last Modified: Wed, 18 Feb 2026 20:12:08 GMT  
		Size: 38.0 MB (37952778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36405ccc7805c78d7a2bd0adcb8859a9211b590bc1e611671f5b30ed8587a811`  
		Last Modified: Wed, 18 Feb 2026 20:12:11 GMT  
		Size: 137.4 MB (137388272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74abe370ded2434015d3349cf37bd1de9988c7a25db98476747c3b48272a05ae`  
		Last Modified: Wed, 18 Feb 2026 20:12:06 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:818190ac44c1c2958b136d27a539baf8d7ae72630198cb622a0ce3b0b7507f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5424879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c9a2e526a5008edc5c177035643d62a2fcfbf51d15200847cd8f477ccd7234`

```dockerfile
```

-	Layers:
	-	`sha256:a871878a49485bf251cb12b7360b0e74959a0f275f9ff28a8059d2cce70d6dee`  
		Last Modified: Wed, 18 Feb 2026 20:12:06 GMT  
		Size: 5.4 MB (5401228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b76536f77b77996424bfc10e3d64557774cef686615a7fb94c9a1f1b4ee21`  
		Last Modified: Wed, 18 Feb 2026 20:12:06 GMT  
		Size: 23.7 KB (23651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:f9a38fe7cf00a6c9b3465051a4a135d013cc2daac31151e7098d6b35bb68a54f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.9 MB (377944511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0712818ec803b9aab37f9346e29fc0edeccad0ca0487a418b0f194c52c15ac39`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL maintainer="Red Hat, Inc."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL vendor="Red Hat, Inc."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL io.openshift.expose-services=""
# Tue, 17 Feb 2026 17:28:18 GMT
LABEL io.openshift.tags="minimal rhel9"
# Tue, 17 Feb 2026 17:28:19 GMT
ENV container oci
# Tue, 17 Feb 2026 17:28:19 GMT
COPY dir:e19a9544af6f4f767332c726437518ba329f6c0cb823e6626d8f737e7b4e03af in /      
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Tue, 17 Feb 2026 17:28:19 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:92884c81bda51cff7047f88f0f2de2d2a1934fb3649e59ef22ffd9a5bdac51d3 in /usr/share/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:28:19 GMT
COPY file:92884c81bda51cff7047f88f0f2de2d2a1934fb3649e59ef22ffd9a5bdac51d3 in /root/buildinfo/labels.json      
# Tue, 17 Feb 2026 17:28:20 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="0ced2bbee24d5463d4530756a57f8db895246c48" "org.opencontainers.image.revision"="0ced2bbee24d5463d4530756a57f8db895246c48" "build-date"="2026-02-17T17:28:07Z" "org.opencontainers.image.created"="2026-02-17T17:28:07Z" "release"="1771346502"org.opencontainers.image.revision=0ced2bbee24d5463d4530756a57f8db895246c48,org.opencontainers.image.created=2026-02-17T17:28:07Z
# Wed, 18 Feb 2026 19:14:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 19:14:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 19:14:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 18 Feb 2026 19:14:16 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Wed, 18 Feb 2026 19:14:16 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Wed, 18 Feb 2026 19:14:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 18 Feb 2026 19:14:30 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 18 Feb 2026 19:14:32 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 18 Feb 2026 19:14:32 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 18 Feb 2026 19:14:32 GMT
CMD ["jshell"]
# Wed, 18 Feb 2026 20:09:51 GMT
CMD ["gradle"]
# Wed, 18 Feb 2026 20:09:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 18 Feb 2026 20:09:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 18 Feb 2026 20:09:51 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 18 Feb 2026 20:09:52 GMT
WORKDIR /home/gradle
# Wed, 18 Feb 2026 20:10:08 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 18 Feb 2026 20:10:08 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 18 Feb 2026 20:10:08 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 18 Feb 2026 20:10:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 18 Feb 2026 20:10:15 GMT
USER gradle
# Wed, 18 Feb 2026 20:10:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 18 Feb 2026 20:10:16 GMT
USER root
```

-	Layers:
	-	`sha256:e49899ec689390291d0a567190cfeebd147dc3fea51e0dc3988e02aceb092cd0`  
		Last Modified: Tue, 17 Feb 2026 18:09:17 GMT  
		Size: 38.1 MB (38128755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44851a32286c38540f8c81cf8d5f76073ac2ac228c91733687399b6124d5fc7`  
		Last Modified: Wed, 18 Feb 2026 19:15:11 GMT  
		Size: 30.4 MB (30415409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3061df060a4d484634cf1bff06d6f3130376b72d0c1d19a5c110dcb25dc167`  
		Last Modified: Wed, 18 Feb 2026 19:15:14 GMT  
		Size: 135.6 MB (135629059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3593c5db569f0556d6d4e6e08d536b02c3f876e592711b8471e3767eaac6eb2`  
		Last Modified: Wed, 18 Feb 2026 19:15:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a5c078d670c891c58d568075afcc227bfab7d63f56d3618b62d3a2423b225`  
		Last Modified: Wed, 18 Feb 2026 19:15:11 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853027853a51bcb70b4a412156d664098bc35313d419c156b44b4d24bd278e68`  
		Last Modified: Wed, 18 Feb 2026 20:10:55 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce32db5fce1e38e7dc4a3aa1c470c034927cce28b49ea53dd17377ee2cd9b237`  
		Last Modified: Wed, 18 Feb 2026 20:10:56 GMT  
		Size: 36.3 MB (36343848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551bb56d12cd593bbd37f1c36988fb2c3975bb9de586bb2b3c6dfaadcd705bac`  
		Last Modified: Wed, 18 Feb 2026 20:10:58 GMT  
		Size: 137.4 MB (137388273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417cb5155f94f27b0c4fbd54b9dbb8aa2270c2cdeeb3b555162d720905bd8170`  
		Last Modified: Wed, 18 Feb 2026 20:10:55 GMT  
		Size: 35.0 KB (35008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:2e11df27e2817902b78a0184597c14b515c4e0fd2b3921afbccf90acbe133a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5414098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65c431b15750222e3ee88687f01e42d1e15edf1936a918641453341aeedd6e2`

```dockerfile
```

-	Layers:
	-	`sha256:d39d25e0e772eb7ed924077559cdeeef16cb97efad863146d16bf72ea6f06229`  
		Last Modified: Wed, 18 Feb 2026 20:10:55 GMT  
		Size: 5.4 MB (5390510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5c35b0991eb06ccaf5424599785797f997cf4387525a0e5aff3c0a5eb45ac99`  
		Last Modified: Wed, 18 Feb 2026 20:10:55 GMT  
		Size: 23.6 KB (23588 bytes)  
		MIME: application/vnd.in-toto+json
