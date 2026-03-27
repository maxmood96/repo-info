## `gradle:jdk21-ubi10`

```console
$ docker pull gradle@sha256:f0be41c178dcf3867655127c3c071aa80a6bb1c8465de06da1653f974a56b265
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

### `gradle:jdk21-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:842ec65ade992c729b78a53c899f644e7bb502c6e160e796f570d7e4dfe6ce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.5 MB (406534392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddc0fa954e674a3a98e42493fee337efc9875638f80d75e743f78966c2a4758`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:20:47 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:20:48 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:20:48 GMT
ENV container oci
# Thu, 26 Mar 2026 17:20:48 GMT
COPY dir:013378efc21240669710b39853c72e001fd6ffb5e0383845178fe8e7ffe47e8f in /      
# Thu, 26 Mar 2026 17:20:48 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:20:48 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:20:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:20:48 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:20:49 GMT
COPY file:f920fc5dc4d46ff47508071b2b2abe21bc425c8efd4d327551b88c78a46db925 in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:20:49 GMT
COPY file:f920fc5dc4d46ff47508071b2b2abe21bc425c8efd4d327551b88c78a46db925 in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:20:49 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:20:31Z" "org.opencontainers.image.created"="2026-03-26T17:20:31Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:20:31Z
# Fri, 27 Mar 2026 18:42:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 18:42:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:42:11 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 18:42:11 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 18:42:11 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 27 Mar 2026 18:43:02 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 18:43:03 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 18:43:03 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 18:43:03 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 18:43:03 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 19:12:19 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 19:12:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 19:12:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 19:12:19 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 19:12:19 GMT
WORKDIR /home/gradle
# Fri, 27 Mar 2026 19:12:23 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 27 Mar 2026 19:12:23 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 27 Mar 2026 19:12:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 27 Mar 2026 19:12:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 27 Mar 2026 19:12:25 GMT
USER gradle
# Fri, 27 Mar 2026 19:12:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 19:12:26 GMT
USER root
```

-	Layers:
	-	`sha256:e6c23a286985c06cc6d9b05d3d1e515a2fe5443b2da741ed6bc423f7907d3e67`  
		Last Modified: Thu, 26 Mar 2026 18:05:52 GMT  
		Size: 34.6 MB (34608408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae11d1549633c5635252da904e6ce7aa6e9acb79dff945086afe3b153cb70015`  
		Last Modified: Fri, 27 Mar 2026 18:42:29 GMT  
		Size: 37.5 MB (37455344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5aea44636994f4143b0df203bebcc6116e3d5168fb5dc79a1993b7a9b1b157b`  
		Last Modified: Fri, 27 Mar 2026 18:43:22 GMT  
		Size: 157.9 MB (157861038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459e0da147591ee3a95026c80d6e90e35e450868cb6c849cad71e6f3e30d41f5`  
		Last Modified: Fri, 27 Mar 2026 18:43:18 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8967c9d3dc68474a9172f9f71f8c058cb02d1f1d51ab50b090776ea5786bb02`  
		Last Modified: Fri, 27 Mar 2026 18:43:19 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5f67e671d39c89ae0230b2960acd9953051a0e22e91bdfe434d2b802705a76`  
		Last Modified: Fri, 27 Mar 2026 19:12:44 GMT  
		Size: 1.6 KB (1581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f2ff9e90238864b24593e8a8e23fa2982fd5311510de8824c70c819b81fd12`  
		Last Modified: Fri, 27 Mar 2026 19:12:46 GMT  
		Size: 38.8 MB (38771615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5badba479adfb9fdb34b9b2dd8bc36c268651c04cf0f36c879b0edab4c9f1e`  
		Last Modified: Fri, 27 Mar 2026 19:12:48 GMT  
		Size: 137.8 MB (137808336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe2f6be882da6ccdb3a125899c7141268285c8f9529c071386138fdd6b344fc`  
		Last Modified: Fri, 27 Mar 2026 19:12:44 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:54e9264faf09857657e52b97fd35994fb03b128837e49e5debd60c41c384aaa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7053231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c0db5ef3cfe5e04baf69941cb7bd196f5f7b78b82575f49c3f2fa46303385a`

```dockerfile
```

-	Layers:
	-	`sha256:b758a68ef23a914a5d8cb6faaab468752bf56695ad28a50d7b8298526106925a`  
		Last Modified: Fri, 27 Mar 2026 19:12:45 GMT  
		Size: 7.0 MB (7028780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f60770952ee4d39f0ca976fc942daf240f4e9cd78da78c70f358ff7d7f4ffaee`  
		Last Modified: Fri, 27 Mar 2026 19:12:44 GMT  
		Size: 24.5 KB (24451 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:98e4f3481c8112ce0c58f1bad861ae2295f8ab07d548daf3a529980704107994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.3 MB (402342531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a92c852cd1655699e3b52d6cf6127a25266ed5c0d9a1ec21a046c21df24eba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:23:52 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:23:52 GMT
ENV container oci
# Thu, 26 Mar 2026 17:23:53 GMT
COPY dir:7d6c6936964da50429cf71ef4747883349075c5f65fea997c68d435e4becb027 in /      
# Thu, 26 Mar 2026 17:23:53 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:23:53 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:23:53 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:23:54 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:23:54 GMT
COPY file:72d28a3a1bd9c93099bf92feb048cbf67d57de2e84328846e17d81fa1ecc79fa in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:23:54 GMT
COPY file:72d28a3a1bd9c93099bf92feb048cbf67d57de2e84328846e17d81fa1ecc79fa in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:23:54 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:23:36Z" "org.opencontainers.image.created"="2026-03-26T17:23:36Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:23:36Z
# Fri, 27 Mar 2026 18:43:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 18:43:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:43:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 18:43:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 18:43:28 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 27 Mar 2026 18:44:01 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 18:44:02 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 18:44:02 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 18:44:02 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 18:44:02 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 19:11:48 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 19:11:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 19:11:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 19:11:48 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 19:11:48 GMT
WORKDIR /home/gradle
# Fri, 27 Mar 2026 19:11:52 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 27 Mar 2026 19:11:52 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 27 Mar 2026 19:11:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 27 Mar 2026 19:11:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 27 Mar 2026 19:11:55 GMT
USER gradle
# Fri, 27 Mar 2026 19:11:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 19:11:56 GMT
USER root
```

-	Layers:
	-	`sha256:3bdc97aa816d30cff74675555d7b3f29b652ed3811ef43aff9bf264de81602f2`  
		Last Modified: Thu, 26 Mar 2026 18:05:46 GMT  
		Size: 32.7 MB (32681363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b56b697405e695d3b65cc0df4ec3a539efd5116b2159b73f51f7b79a7744452`  
		Last Modified: Fri, 27 Mar 2026 18:43:47 GMT  
		Size: 37.4 MB (37405287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26687f1dc2db84cf2129d256a1846cf07406e5f8f2231cc6510e3d4a5f1bb04c`  
		Last Modified: Fri, 27 Mar 2026 18:44:22 GMT  
		Size: 156.1 MB (156136310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb9713eaa570e31268a86d6f215eef89acf235a0790dafa4049b6703f33bf61`  
		Last Modified: Fri, 27 Mar 2026 18:44:19 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7369b2328087c29633d716e11ae713df761d582d6d1b10c2ffedd0d6ec535e85`  
		Last Modified: Fri, 27 Mar 2026 18:44:19 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e8d9f861beb1aae77912cec635894cf75fe6b5e1c8a60856b2add3aa7a4a27`  
		Last Modified: Fri, 27 Mar 2026 19:12:14 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6677e544fb1e9fefe5b62751236ce397879e73ede0d40f2e087d567b41ea925b`  
		Last Modified: Fri, 27 Mar 2026 19:12:16 GMT  
		Size: 38.3 MB (38277860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94122cf6ba1b96be547036c19fc04fc59b593eda78484eab09fb2dfd0e5d085`  
		Last Modified: Fri, 27 Mar 2026 19:12:19 GMT  
		Size: 137.8 MB (137808334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a654fcc659524c64dd1a692edf4d3e6e52a08acc027c63b99f767f79650c251b`  
		Last Modified: Fri, 27 Mar 2026 19:12:14 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:3b0793c2a333a84ff35d42c22049a70414e6dd633fd08dec35a76fc00f0072c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7051684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd07ce9e23d11cb9404bc5fdde374d79474df804ed63abb53c5ab4fc18691f9`

```dockerfile
```

-	Layers:
	-	`sha256:bb1bd45c59261f614991d8eb1f552afec8497dffab20fe3239fc03074acf6a3a`  
		Last Modified: Fri, 27 Mar 2026 19:12:15 GMT  
		Size: 7.0 MB (7027036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bab4f41f60ea966ccf1d1e12e5514b076b6f31269e8937d20958cd65492e8c`  
		Last Modified: Fri, 27 Mar 2026 19:12:14 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:4410dfcce87ab7a7e82f91587bf25cdfe4a8a3f892fea67d58a24d783a538b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.2 MB (414226293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871113da3a0f4883e46890f8c566029f6d444690d43d87458ba69ef1c2ed8982`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:22:03 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:22:03 GMT
ENV container oci
# Thu, 26 Mar 2026 17:22:03 GMT
COPY dir:c58a58aa30d2fc124efbb2fad87948342334ec1169d24c59d7c515f23167fc05 in /      
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:22:04 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:dd5a12247eaa56c1bce4445e2f72f6ec10e514179740b9b280ada967bb02c904 in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:22:04 GMT
COPY file:dd5a12247eaa56c1bce4445e2f72f6ec10e514179740b9b280ada967bb02c904 in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:22:04 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:21:51Z" "org.opencontainers.image.created"="2026-03-26T17:21:51Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:21:51Z
# Fri, 27 Mar 2026 19:25:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 19:25:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 19:25:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 19:25:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 19:25:44 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 27 Mar 2026 19:28:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 19:28:52 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 19:28:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 19:28:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 19:28:53 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 20:09:30 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 20:09:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 20:09:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 20:09:30 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 20:09:31 GMT
WORKDIR /home/gradle
# Fri, 27 Mar 2026 20:09:49 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 27 Mar 2026 20:09:49 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 27 Mar 2026 20:09:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 27 Mar 2026 20:09:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 27 Mar 2026 20:09:57 GMT
USER gradle
# Fri, 27 Mar 2026 20:09:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 20:09:59 GMT
USER root
```

-	Layers:
	-	`sha256:d3afc82808d99ce4baa1bde62af82befcf71b8d6cb81303429e8a1936966a71f`  
		Last Modified: Thu, 26 Mar 2026 18:15:14 GMT  
		Size: 38.7 MB (38703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ff6796efd7123f48d41ed631253b9606a3787b30627617e5128dcacafc4e44`  
		Last Modified: Fri, 27 Mar 2026 19:26:28 GMT  
		Size: 39.2 MB (39215080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c75a414e45e391dfd71393d85b22875f9ec5ee2f29ecdca69a19fa2f07aab4b`  
		Last Modified: Fri, 27 Mar 2026 19:29:33 GMT  
		Size: 158.0 MB (157981374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414eb02ed3101578412944e2a4ee4f79c4e55e219fb9ed4de561f193dbaec63c`  
		Last Modified: Fri, 27 Mar 2026 19:29:29 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cc5ebac5d9ca85b438ed0f4e3fc8c49839985e66dae23c5d5b605e5be38475`  
		Last Modified: Fri, 27 Mar 2026 19:29:29 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e61da55199bc50b36d6262f26f6b6a4a449d0b0c83cd6862d447c8ed026e6`  
		Last Modified: Fri, 27 Mar 2026 20:10:42 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036f6a3359d644e688c895a4046729c37904a9695b5fdd19bbcd7edc9eece058`  
		Last Modified: Fri, 27 Mar 2026 20:10:44 GMT  
		Size: 40.5 MB (40513677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5bd56cf93737cf65e83a8f8b0ff072a6ecc71f5cd1bbf5527eab6540e978b7`  
		Last Modified: Fri, 27 Mar 2026 20:10:46 GMT  
		Size: 137.8 MB (137808334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fb2467be357809901c3186085567aee62dbd687d3c7c0f16134af7c6d227d3`  
		Last Modified: Fri, 27 Mar 2026 20:10:42 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:21303d9f7adba5334f60ac9ff8154c6886778c6de91771e00c6352c7707dd51c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7044720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9537f43051b255373805b66eadab89712af7fa16d4a8c111fb24774137f8f58a`

```dockerfile
```

-	Layers:
	-	`sha256:8f1c2718de421605fade60215be0f1fb1c28bc899eba323fde9171c948ad4778`  
		Last Modified: Fri, 27 Mar 2026 20:10:42 GMT  
		Size: 7.0 MB (7020198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2680fac8dbf656507326d3b2451e513a80fb7bdca17feb2979d7ca167ebf9150`  
		Last Modified: Fri, 27 Mar 2026 20:10:42 GMT  
		Size: 24.5 KB (24522 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:e707e0b0c7ca5f487e715d394974ee5a41d5923c9abdd8d54a54dcdfbabe9a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.1 MB (398062085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b32ab2e1406ba051c10d0434d4df21e2e608a6312d48476e1dd40b7547506ba`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.1"       cpe="cpe:/o:redhat:enterprise_linux:10.1"       distribution-scope="public"
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL io.openshift.expose-services=""
# Thu, 26 Mar 2026 17:28:54 GMT
LABEL io.openshift.tags="minimal rhel10"
# Thu, 26 Mar 2026 17:28:55 GMT
ENV container oci
# Thu, 26 Mar 2026 17:28:55 GMT
COPY dir:94a3048ecdc388a9fe69dc605a5ee32b82678da3107c34d9f886aca0d5d2e171 in /      
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Thu, 26 Mar 2026 17:28:55 GMT
CMD ["/bin/bash"]
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:4fd670c85c1bcf73f03c7e85a75e911c58dd6829a2070a9da8f858286ab68657 in /usr/share/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:28:55 GMT
COPY file:4fd670c85c1bcf73f03c7e85a75e911c58dd6829a2070a9da8f858286ab68657 in /root/buildinfo/labels.json      
# Thu, 26 Mar 2026 17:28:56 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="4d17df4ea3ff25815cca2550bc445280420af0a9" "org.opencontainers.image.revision"="4d17df4ea3ff25815cca2550bc445280420af0a9" "build-date"="2026-03-26T17:28:13Z" "org.opencontainers.image.created"="2026-03-26T17:28:13Z" "release"="1774545417"org.opencontainers.image.revision=4d17df4ea3ff25815cca2550bc445280420af0a9,org.opencontainers.image.created=2026-03-26T17:28:13Z
# Fri, 27 Mar 2026 18:58:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 18:58:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:58:46 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 18:58:46 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 18:58:46 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Fri, 27 Mar 2026 18:59:55 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='357fee29fb0d5c079f6730db98b28942df13a6eed426f6c61cd4ad703ab27b9a';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.10_7.tar.gz';          ;;        ppc64le)          ESUM='33bdaec351f40cc70d44e251a54c23e4dd15fed8adc041e35c57461c706cf948';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.10_7.tar.gz';          ;;        s390x)          ESUM='eabb069b59a2e6b9e9926d9c533186aabf1ff3b4af683d0a3620bb7c7d9770c0';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.10_7.tar.gz';          ;;        x86_64)          ESUM='ea3b9bd464d6dd253e9a7accf59f7ccd2a36e4aa69640b7251e3370caef896a4';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jdk_x64_linux_hotspot_21.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 18:59:57 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 18:59:57 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 18:59:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 18:59:57 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 19:10:33 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 19:10:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 19:10:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 19:10:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 19:10:33 GMT
WORKDIR /home/gradle
# Fri, 27 Mar 2026 19:10:40 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 27 Mar 2026 19:10:40 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 27 Mar 2026 19:10:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 27 Mar 2026 19:10:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 27 Mar 2026 19:10:43 GMT
USER gradle
# Fri, 27 Mar 2026 19:10:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 19:10:44 GMT
USER root
```

-	Layers:
	-	`sha256:9c01cab36040f3f8f1c78284c2d60452730d51f09eb8623c854a44417db02f17`  
		Last Modified: Thu, 26 Mar 2026 18:15:05 GMT  
		Size: 34.4 MB (34434323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc8e9d144776fa7c71dee43cd87d4af1806a05210b7ea8e2fd16073b8bf5477`  
		Last Modified: Fri, 27 Mar 2026 18:59:17 GMT  
		Size: 37.8 MB (37834995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5607fbbcf2e20bc6203b642094cd357660fde9c68af53bdaafd2b5ff845c995a`  
		Last Modified: Fri, 27 Mar 2026 19:00:24 GMT  
		Size: 147.1 MB (147104844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f01b50c6e10052cb13d8e489cd11adeede9169e2996a876c819ac79efd4e40c`  
		Last Modified: Fri, 27 Mar 2026 19:00:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee4d1426a8c6992db6181f72b528d1d4b1388b8d4980b874436d1e72cecb13a`  
		Last Modified: Fri, 27 Mar 2026 19:00:22 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111074ef72519d193295ed533f2090e901d935d446e8f4ff91b726c0f0f0eaad`  
		Last Modified: Fri, 27 Mar 2026 19:11:15 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3b7ffcd5dbdd8c0b9b82bdc13cb4bea28af2174233560d5fa6f86677484560`  
		Last Modified: Fri, 27 Mar 2026 19:11:16 GMT  
		Size: 40.9 MB (40875177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0879e8a35f5d014ce9f02797f63b033554b4b4011f670efa4c8e3374eda0a6`  
		Last Modified: Fri, 27 Mar 2026 19:11:18 GMT  
		Size: 137.8 MB (137808333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f9271ab6af1b13d67f8e399b85447d29ce3b8f05ab057bb2b96ede91049f19`  
		Last Modified: Fri, 27 Mar 2026 19:11:15 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:f6d076da082e05618d84608a326f61f112782b8ff40de50c73fd06ec40443aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7033876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab918839809196bed6f8bffea57d34cdfb6b07171b7d82439d50d51a961b606`

```dockerfile
```

-	Layers:
	-	`sha256:c453048341bc9c38a559c5d98a59c792808d5ca334f2bc7e0924ed10af295e71`  
		Last Modified: Fri, 27 Mar 2026 19:11:15 GMT  
		Size: 7.0 MB (7009427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42d96076d51b614b10a2667ee249da8504fa3f4e36722f05405f9a84dd453083`  
		Last Modified: Fri, 27 Mar 2026 19:11:15 GMT  
		Size: 24.4 KB (24449 bytes)  
		MIME: application/vnd.in-toto+json
