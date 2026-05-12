## `gradle:8-jdk21-ubi`

```console
$ docker pull gradle@sha256:dc100e38ed1becd9ea452a741205e661dfe0a27004d01c4e79af8da451df0147
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

### `gradle:8-jdk21-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:c75c2dccf192f4cff68508b907c8f8be06826161f1414dd65089dceaa4346f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403357497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b559114e328c362ddc1d4b62f357faf707a90d014c8620f92b6bbf44ead606`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:07:55 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:07:55 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:07:55 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:07:55 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:07:55 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:07:55 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:07:55 GMT
ENV container oci
# Mon, 11 May 2026 01:07:56 GMT
COPY dir:d396e6c334ec17a1ba4a03f21481f526666f77d114978313ef1df55edd8e1412 in /      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:07:56 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:56 GMT
COPY file:1b5a90f3ed08efd6f44de46e666565e2a9b8e1a168d7a249c016b23dc19bcaac in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:07:57 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:07:39Z" "org.opencontainers.image.created"="2026-05-11T01:07:39Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:07:39Z
# Tue, 12 May 2026 00:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:03:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:03:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:03:44 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:05:13 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:05:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:05:14 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:05:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:05:14 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:17:27 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:17:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:17:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:17:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:17:27 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:17:31 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:17:31 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 12 May 2026 00:17:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 12 May 2026 00:18:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:18:05 GMT
USER gradle
# Tue, 12 May 2026 00:18:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:18:05 GMT
USER root
```

-	Layers:
	-	`sha256:34f4a557df8123a31168a9ed57304a4ee0a79b26712d1770dcf7c798372b100b`  
		Last Modified: Mon, 11 May 2026 02:10:30 GMT  
		Size: 40.0 MB (39994724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38de3c3bb095f10d951999805aae95621256a5093a2e831bab5cf51b603f636`  
		Last Modified: Tue, 12 May 2026 00:04:01 GMT  
		Size: 30.4 MB (30369082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a46ed015722792946ed8863942d677be26cbc9dd5fcd0992a3c329c07d40d36`  
		Last Modified: Tue, 12 May 2026 00:05:35 GMT  
		Size: 158.2 MB (158172682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10699f3e26325d256f0df96b0ab7cd076161018e9ad106c16d2d52654ca1bd10`  
		Last Modified: Tue, 12 May 2026 00:05:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ddb6b59eb80f4653eda5427d8a7e3d3248532874836caabba20c2dc1064d22`  
		Last Modified: Tue, 12 May 2026 00:05:30 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e22f26d01403c08912f07cf72313c484f3f54419d14f5b722a0dee578c7bf38`  
		Last Modified: Tue, 12 May 2026 00:17:50 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b375fb1da00a68079bd560a7ad835bab82f46a913ff31b1b535ff2057208cfd`  
		Last Modified: Tue, 12 May 2026 00:17:53 GMT  
		Size: 36.7 MB (36693371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089560a3e674ff3aa41573306d59058850334b71cea873a9ed214f1dee41fc36`  
		Last Modified: Tue, 12 May 2026 00:18:23 GMT  
		Size: 138.1 MB (138068581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899539f2d40634f01f802adde2df82b553fda10b903a7096856359a40bd9434f`  
		Last Modified: Tue, 12 May 2026 00:18:19 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1c78b62c1669c2e3792326de0931659b759417a7a223d978b6f75b42bf0117ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5430282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d81c4bd358b1bf0f14d4beac6369957be26e7e7d6d1d16db4c10134a5a1f52d`

```dockerfile
```

-	Layers:
	-	`sha256:369c928ca63da667eca0a97f5d17692e29ac90748dcd2862fe556ff2e00f4b77`  
		Last Modified: Tue, 12 May 2026 00:18:20 GMT  
		Size: 5.4 MB (5406402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34738e8c4afea5a0dc2c384efed70878a461601a4792f8f4cff8aa731fe571e3`  
		Last Modified: Tue, 12 May 2026 00:18:19 GMT  
		Size: 23.9 KB (23880 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:02d4ffa5d20880ad94b2b1d059fe6b1c0e07551b755dec7c5109c06f2f52022b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.6 MB (399618067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e73705db7ab6e55368064889edc2c9e32f0335989e758a000552dbf079857d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:10:03 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:10:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:10:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:10:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:10:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:10:04 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:10:04 GMT
ENV container oci
# Mon, 11 May 2026 01:10:05 GMT
COPY dir:f96b78a7f24437106ae6a323adf2c06c98f78157637998e58adf24d336fc59f9 in /      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:10:05 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
COPY file:4815587a81c6816403ce960a517de92d74cd550eeda95c6164f5b3614ab4c3fe in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:05 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:09:50Z" "org.opencontainers.image.created"="2026-05-11T01:09:50Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:09:50Z
# Mon, 11 May 2026 23:59:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 11 May 2026 23:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:59:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 11 May 2026 23:59:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 11 May 2026 23:59:46 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:03:16 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:03:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:03:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:03:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:03:17 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:17:20 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:17:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:17:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:17:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:17:20 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:17:23 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:17:23 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 12 May 2026 00:17:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 12 May 2026 00:17:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:17:26 GMT
USER gradle
# Tue, 12 May 2026 00:17:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:17:27 GMT
USER root
```

-	Layers:
	-	`sha256:07b48350f3398d184075c56877eb97837294903946c9a6c10031807b6c4f549d`  
		Last Modified: Mon, 11 May 2026 02:11:01 GMT  
		Size: 38.2 MB (38205518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd6ab7ec1d6210314e91ddca10dab2e77942a0ef57b3d2cad8094a806f34c10`  
		Last Modified: Tue, 12 May 2026 00:00:08 GMT  
		Size: 30.8 MB (30789492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91519b8811e5c63563e8e9cf3c8b4d0800ea5928cc1f3ca79a252f1b4cac696e`  
		Last Modified: Tue, 12 May 2026 00:03:38 GMT  
		Size: 156.5 MB (156464375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f452f52b93bfedcdbcdbcba994ffac305623e34ea35bb87256d4af91dd0df632`  
		Last Modified: Tue, 12 May 2026 00:03:34 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860aa0395924bbdb7056e310c70c31316c63c16660ba28b50990c2805e47da03`  
		Last Modified: Tue, 12 May 2026 00:03:34 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171cee5b6fa5c32743bdb71250cfeec4c7cbbec9e3370c95f03b2c03de47b91`  
		Last Modified: Tue, 12 May 2026 00:17:43 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf518bff0a479883e594ff004e3533315e990181c8df56664e956d49c176896`  
		Last Modified: Tue, 12 May 2026 00:17:45 GMT  
		Size: 36.0 MB (36026402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ba02598fe4d4137c3160becc7c9119f19eebc8019ad5dba841e425c531a692`  
		Last Modified: Tue, 12 May 2026 00:17:47 GMT  
		Size: 138.1 MB (138068570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8e04172a76d4445108bcf93f275a765ad31b7435c66fc96e9d5243acad6528`  
		Last Modified: Tue, 12 May 2026 00:17:43 GMT  
		Size: 59.5 KB (59549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:56eaa28b5c93ca784fa438864d20c84cb17ceeb96671bf1b141fad576096324a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5429860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe9395df24a10abd3d5295358f70283eb3d2e3dfcb016b5268305f40511d2e6`

```dockerfile
```

-	Layers:
	-	`sha256:9545aef63b862705df9cfbec787a8576e28d2edc78bc7cc4c61ffefac8cbb60b`  
		Last Modified: Tue, 12 May 2026 00:17:44 GMT  
		Size: 5.4 MB (5405808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b5967fde8d245bac914743b000a50951d377e3478ef8c1ef5f62d0c43e2840`  
		Last Modified: Tue, 12 May 2026 00:17:43 GMT  
		Size: 24.1 KB (24052 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:cad8b99cba193da315609f18cbd3aa2ec4b1c633cda6a8c940886793124630e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411679211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d79cdda7b236f018cd8bc76f7e07e39d63324b0d4be1d4253ebdefec2056350`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 06 May 2026 12:56:35 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 06 May 2026 12:56:35 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 06 May 2026 12:56:35 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 06 May 2026 12:56:35 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Wed, 06 May 2026 12:56:35 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 06 May 2026 12:56:35 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 06 May 2026 12:56:35 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.openshift.expose-services=""
# Wed, 06 May 2026 12:56:35 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 06 May 2026 12:56:35 GMT
ENV container oci
# Wed, 06 May 2026 12:56:36 GMT
COPY dir:80e7e7cac97ce232e3c4b678751f9a2b11cc4a26beaae93a957f83f1fc548f95 in /      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Wed, 06 May 2026 12:56:36 GMT
CMD ["/bin/bash"]
# Wed, 06 May 2026 12:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:bffe3875426b01ab6d752ed5055c4e2d920bf40e31b44b873a80786da1d0750b in /usr/share/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:36 GMT
COPY file:bffe3875426b01ab6d752ed5055c4e2d920bf40e31b44b873a80786da1d0750b in /root/buildinfo/labels.json      
# Wed, 06 May 2026 12:56:37 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "org.opencontainers.image.revision"="8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c" "build-date"="2026-05-06T12:56:25Z" "org.opencontainers.image.created"="2026-05-06T12:56:25Z" "release"="1778072020"org.opencontainers.image.revision=8def05a6f0dfabdc25ea20a79b0d11f8f9b12c5c,org.opencontainers.image.created=2026-05-06T12:56:25Z
# Fri, 08 May 2026 16:18:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 16:18:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 16:18:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 08 May 2026 16:18:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 08 May 2026 16:18:41 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 16:24:53 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 08 May 2026 16:24:56 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 08 May 2026 16:24:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 08 May 2026 16:24:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 08 May 2026 16:24:57 GMT
CMD ["jshell"]
# Fri, 08 May 2026 16:40:42 GMT
CMD ["gradle"]
# Fri, 08 May 2026 16:40:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 08 May 2026 16:40:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 08 May 2026 16:40:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 08 May 2026 16:40:42 GMT
WORKDIR /home/gradle
# Fri, 08 May 2026 16:41:04 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 08 May 2026 16:41:04 GMT
ENV GRADLE_VERSION=8.14.5
# Fri, 08 May 2026 16:41:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Fri, 08 May 2026 20:05:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 08 May 2026 20:05:57 GMT
USER gradle
# Fri, 08 May 2026 20:05:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 08 May 2026 20:05:59 GMT
USER root
```

-	Layers:
	-	`sha256:e3c3e69dacc2a761a2218333f5a3c6de6e1ae1b3afa56e02bcb3f2e70f91db2c`  
		Last Modified: Wed, 06 May 2026 18:13:19 GMT  
		Size: 44.5 MB (44456866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30e4b2f46114bf6e128a1cbe09e30dd7493dd7f6692477ad27cf63291c7e84f`  
		Last Modified: Fri, 08 May 2026 16:19:19 GMT  
		Size: 32.8 MB (32843917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7e96fc5e89a6683c8e78548a7d69a6db44fd8717c5e29dbfc5285afe5011b7`  
		Last Modified: Fri, 08 May 2026 16:25:38 GMT  
		Size: 158.3 MB (158348498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff08625fff91d084eef5517739f1640e55d159cf4452cc60930a3ffbf93bc1`  
		Last Modified: Fri, 08 May 2026 16:25:33 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a572dd8b14a4765f6c6b1d7cbdcb4666d0f47e9e2d2cffd2ed530bc86ccd458`  
		Last Modified: Fri, 08 May 2026 16:25:34 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e027a5be4198b5775e0f1ad1ffd5d3f32d8b4303cc578c1f9f4fdae0bd3c87ab`  
		Last Modified: Fri, 08 May 2026 16:42:04 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d60ea063183ff0ada9478066f06f5f369738b50fc59ece5ff030ef4e85328fd`  
		Last Modified: Fri, 08 May 2026 16:42:06 GMT  
		Size: 37.9 MB (37922213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caf1c9fceac64b0b3ee9d4f81339dfe4d5009a4599a4f462038e926781da205`  
		Last Modified: Fri, 08 May 2026 20:06:41 GMT  
		Size: 138.1 MB (138068540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2edc28fdff8cb1cf281b2cc628187f655bebf5d628192bad5cee51fc1aa52c5`  
		Last Modified: Fri, 08 May 2026 20:06:36 GMT  
		Size: 35.0 KB (35013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:e53bcbc93fd9f7ba7a793c8fac6c0b9eee13fc37b30727ae69d30ed8b8b394b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5427665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af64475c8b7aa8a8a3fe3ce4a8810ff77224c429a6552b166acc6eb23f8f2102`

```dockerfile
```

-	Layers:
	-	`sha256:1ad383fa82ff65d053f2174b9287fa9ef884cada32f9eed6aecdf43c74f2b30b`  
		Last Modified: Fri, 08 May 2026 20:06:36 GMT  
		Size: 5.4 MB (5403723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa491d6e5cc0d36e312f5218f2be5a2c0bec91e57ddde565a6fe75fe5d4bb6ad`  
		Last Modified: Fri, 08 May 2026 20:06:36 GMT  
		Size: 23.9 KB (23942 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:d319df88c111c42dd8f98ab4d2aee3b6c3764b334ad7cafd431f9a1bb44616a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390342358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b614c387f9a750873ee4e2f3e5387bb62a1aa2fe2a306a1459087ad0667ae42`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 11 May 2026 01:10:09 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 11 May 2026 01:10:09 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 11 May 2026 01:10:09 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 11 May 2026 01:10:09 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 11 May 2026 01:10:09 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 11 May 2026 01:10:09 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 11 May 2026 01:10:09 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:09 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 11 May 2026 01:10:09 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 11 May 2026 01:10:09 GMT
LABEL io.openshift.expose-services=""
# Mon, 11 May 2026 01:10:09 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 11 May 2026 01:10:09 GMT
ENV container oci
# Mon, 11 May 2026 01:10:10 GMT
COPY dir:2a2bb91993c7787b85a3cdef17fac2d4a451771711ace3d2f7d4a57df4fd720e in /      
# Mon, 11 May 2026 01:10:10 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 11 May 2026 01:10:10 GMT
CMD ["/bin/bash"]
# Mon, 11 May 2026 01:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 11 May 2026 01:10:10 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 11 May 2026 01:10:10 GMT
COPY file:6e6aef2633a1aeb29df36766e5920d63b41f2443841821a183adbf53bfc02d4f in /usr/share/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:10 GMT
COPY file:6e6aef2633a1aeb29df36766e5920d63b41f2443841821a183adbf53bfc02d4f in /root/buildinfo/labels.json      
# Mon, 11 May 2026 01:10:10 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "org.opencontainers.image.revision"="15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1" "build-date"="2026-05-11T01:09:59Z" "org.opencontainers.image.created"="2026-05-11T01:09:59Z" "release"="1778461551"org.opencontainers.image.revision=15c06b7b1c40ffa5f97dc04e88d2d76dc1a15bc1,org.opencontainers.image.created=2026-05-11T01:09:59Z
# Tue, 12 May 2026 00:00:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 00:00:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:00:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 12 May 2026 00:00:27 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 12 May 2026 00:00:27 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Tue, 12 May 2026 00:02:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 12 May 2026 00:02:26 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 12 May 2026 00:02:26 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 12 May 2026 00:02:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 12 May 2026 00:02:26 GMT
CMD ["jshell"]
# Tue, 12 May 2026 00:13:53 GMT
CMD ["gradle"]
# Tue, 12 May 2026 00:13:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 00:13:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 00:13:53 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 00:13:53 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 00:13:58 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 12 May 2026 00:13:58 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 12 May 2026 00:13:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 12 May 2026 00:14:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 00:14:01 GMT
USER gradle
# Tue, 12 May 2026 00:14:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 00:14:02 GMT
USER root
```

-	Layers:
	-	`sha256:9e318380099430c4b5b0b9ce404e5438a459390bacd9fa537031869a73d98e4b`  
		Last Modified: Mon, 11 May 2026 06:12:10 GMT  
		Size: 38.1 MB (38128501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e91c90ce3db8a8b54c33928da91ec2124d42bb6f3f4ce2819ab15e28876fab`  
		Last Modified: Tue, 12 May 2026 00:00:56 GMT  
		Size: 30.4 MB (30382364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f5d8ff2c08b7e02ef530e84dbc13e7ff3dbf8ba42f9341230d93c7e64b52fb`  
		Last Modified: Tue, 12 May 2026 00:02:51 GMT  
		Size: 147.4 MB (147390157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc6169121e749170ada30890ab19298dbb021e3dc052ae33baf56c8ab9ac98c`  
		Last Modified: Tue, 12 May 2026 00:02:48 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32cc5e2e407e3cf3b4dfd014886c3a5949d9bbbbaeed2e3c3a766ecc794a961`  
		Last Modified: Tue, 12 May 2026 00:02:48 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339864d947c3e6500b9f0bdb9d7cbd957c38ec4d822f774172974c9662ce6f5a`  
		Last Modified: Tue, 12 May 2026 00:14:28 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49bb0a0bf435a4b74a1e02740ccc61a507111983627e4c2cdf988433d208d1d`  
		Last Modified: Tue, 12 May 2026 00:14:29 GMT  
		Size: 36.3 MB (36333585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521801983dfcb2c7190d4e4b6058e52aa0f1837cefed7a045a458ebf8394baa4`  
		Last Modified: Tue, 12 May 2026 00:14:30 GMT  
		Size: 138.1 MB (138068578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708a4b2fff37acd65e823d0e80ba507cd6f8cb900cfcc6135175d0c306debe4e`  
		Last Modified: Tue, 12 May 2026 00:14:27 GMT  
		Size: 35.0 KB (35011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:2a1e3f5eb9e89ee2f8518d0264db20fc05553703d6aa6e1250b2abb07e44147b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5416887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f4ffcc031afe832b83f55bb4df00091405d5f83442ef94a2530c95851a2e40`

```dockerfile
```

-	Layers:
	-	`sha256:16cdea5e00f3ec754da7d03c51475123fb4d47b4d9dda8a7a9b6332821bd4ce1`  
		Last Modified: Tue, 12 May 2026 00:14:28 GMT  
		Size: 5.4 MB (5393007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3948c87389301b6b3c633158fef84209cad62c814a1446cb5a8b6f0ac7a4636e`  
		Last Modified: Tue, 12 May 2026 00:14:28 GMT  
		Size: 23.9 KB (23880 bytes)  
		MIME: application/vnd.in-toto+json
