## `gradle:9-jdk17-ubi10`

```console
$ docker pull gradle@sha256:87b9d8ea7accefd0e0aa45681e404e639ecabe3f85e764ca68d948f910462540
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

### `gradle:9-jdk17-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:6400f6f8568a492988416986ab42c29b459f12981e1f8673ad945c88d328e741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 MB (394310327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83454cc5f0ae7201ad7e6b64fc3496d3cefde88b3098143af1412fb3b732fa1`
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
# Fri, 27 Mar 2026 18:42:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 18:42:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:42:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 18:42:41 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 18:42:41 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Fri, 27 Mar 2026 18:42:47 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 18:42:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 18:42:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 18:42:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 18:42:48 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 19:12:18 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 19:12:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 19:12:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 19:12:18 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 19:12:18 GMT
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
# Fri, 27 Mar 2026 19:12:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 19:12:25 GMT
USER root
```

-	Layers:
	-	`sha256:e6c23a286985c06cc6d9b05d3d1e515a2fe5443b2da741ed6bc423f7907d3e67`  
		Last Modified: Thu, 26 Mar 2026 18:05:52 GMT  
		Size: 34.6 MB (34608408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc04146b88166549ce65019eb36f862dce743ae7bd8b4c3328ee3f405f22206`  
		Last Modified: Fri, 27 Mar 2026 18:43:07 GMT  
		Size: 37.5 MB (37455228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf690386144d3bc45b1531842043512e0b47a0dada1fc836750bbf294d780c9d`  
		Last Modified: Fri, 27 Mar 2026 18:43:09 GMT  
		Size: 145.6 MB (145637158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43a6971cefa145f0141d41bdac946f47178e06600342bd0e752428bfa197e3d`  
		Last Modified: Fri, 27 Mar 2026 18:43:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6590c21c27b84117ec0047af827455350e3ced4cfc74d883dfc774043b2b6d`  
		Last Modified: Fri, 27 Mar 2026 18:42:49 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c6450924a5d026819969c4a3d5300b96642c4b2001143b275e82bb858e7916`  
		Last Modified: Fri, 27 Mar 2026 19:12:44 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88bbeeabefc6612cb8479f5e4e7d83b2ae998c13a8df4f0e5415a444750c8c1`  
		Last Modified: Fri, 27 Mar 2026 19:12:47 GMT  
		Size: 38.8 MB (38771550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987616fd7b7ee4c94cec87d5017cf688445618679ed7376304306d1ff52a79ee`  
		Last Modified: Fri, 27 Mar 2026 19:12:49 GMT  
		Size: 137.8 MB (137808337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9893a7fe0918c3c425a4635593b1bc9e4e2db96dbe720651ffce8b57d2f8f471`  
		Last Modified: Fri, 27 Mar 2026 19:12:44 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:753d1d2010531b4a21aee4ea5a25501d6f4d2801f5d493f6aa31ac5c046004cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7051378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b1849159cd3c06d1a9c83df0bc7551aef22e6e4ec3b37aa6653783240c1164`

```dockerfile
```

-	Layers:
	-	`sha256:4b22d59d8052e54493a64d958ef05efbd9b20967ff5ceaa0cc69012259d47a74`  
		Last Modified: Fri, 27 Mar 2026 19:12:45 GMT  
		Size: 7.0 MB (7026928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4be645928ee6183133a956d4936df6ce85be1e73d174e765554f129e368810c`  
		Last Modified: Fri, 27 Mar 2026 19:12:44 GMT  
		Size: 24.4 KB (24450 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cf3c0cb264d1e5127ae52416a293b1247aa60f3891a16ae15f104193c7b94354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.7 MB (390652949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8d3ab33b76de8a7bd2853fc20222f0b74e6d9740abf07e38afa2f90feb8a8d`
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
ENV JAVA_VERSION=jdk-17.0.18+8
# Fri, 27 Mar 2026 18:43:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 18:43:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 18:43:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 18:43:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 18:43:59 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 19:12:11 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 19:12:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 19:12:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 19:12:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 19:12:11 GMT
WORKDIR /home/gradle
# Fri, 27 Mar 2026 19:12:15 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 27 Mar 2026 19:12:15 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 27 Mar 2026 19:12:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 27 Mar 2026 19:12:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 27 Mar 2026 19:12:18 GMT
USER gradle
# Fri, 27 Mar 2026 19:12:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 19:12:18 GMT
USER root
```

-	Layers:
	-	`sha256:3bdc97aa816d30cff74675555d7b3f29b652ed3811ef43aff9bf264de81602f2`  
		Last Modified: Thu, 26 Mar 2026 18:05:46 GMT  
		Size: 32.7 MB (32681363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03d6e6712ba266e8ac6b6897c35706b11909b7e784af2ecda3228710ff7a12d`  
		Last Modified: Fri, 27 Mar 2026 18:43:45 GMT  
		Size: 37.4 MB (37405334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f94a4eae50739a2a21988f337370af689e446a3a3f2e6e96c2d778f24291ee1`  
		Last Modified: Fri, 27 Mar 2026 18:44:19 GMT  
		Size: 144.4 MB (144446622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f7b72a9d56871b0409f2c116dc44ef437b48f27974f1c8244ce19c8e92ad31`  
		Last Modified: Fri, 27 Mar 2026 18:44:15 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbfb6091fb818e1349f25755fc336df31c072d42ead0c34600191903b7ca0d`  
		Last Modified: Fri, 27 Mar 2026 18:44:15 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e24acb1b9a04ed4a973adade5f8e417f0aba618df716729590bda85054fe04`  
		Last Modified: Fri, 27 Mar 2026 19:12:38 GMT  
		Size: 1.6 KB (1585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9231d45b424e9d43ffe732f7fccb284818bebc325e20b38313212dea62570c`  
		Last Modified: Fri, 27 Mar 2026 19:12:39 GMT  
		Size: 38.3 MB (38277919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1253d6d125ff3ace617533d0feec9a2f6267bc55c87c6486236d28e632af7718`  
		Last Modified: Fri, 27 Mar 2026 19:12:41 GMT  
		Size: 137.8 MB (137808336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cbda821d01824061af188684c1ee889f811b4bbe81c740c0952c4ea0e79e31`  
		Last Modified: Fri, 27 Mar 2026 19:12:37 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:def9bccf395be168772d05ce3dd7618cadb4bb1c7309d19bbf49350c623fd811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7049832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2847f9e2f3217ecdf9fd6d6cbcd5733bc02a703dbb406620eee6ce96e7754af`

```dockerfile
```

-	Layers:
	-	`sha256:9af976b7ccda286a6d3c56264cf20440cd36f8953193a0363e177d9f1911c80a`  
		Last Modified: Fri, 27 Mar 2026 19:12:38 GMT  
		Size: 7.0 MB (7025184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f990b7b18debd4d2e800d59f91a12293a92b546775e5b7449a189cab6b6621`  
		Last Modified: Fri, 27 Mar 2026 19:12:37 GMT  
		Size: 24.6 KB (24648 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:85606b73b9545ac353d812a45183ed806125f1359c646b3dfb8602081294e288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.7 MB (401704904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa5ce3c7d96c879ae168dc4e92b47c741fbeae2a76c67a15e546fdc00542e31`
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
ENV JAVA_VERSION=jdk-17.0.18+8
# Fri, 27 Mar 2026 19:27:45 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 19:27:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 19:27:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 19:27:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 19:27:49 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 20:11:01 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 20:11:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 20:11:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 20:11:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 20:11:02 GMT
WORKDIR /home/gradle
# Fri, 27 Mar 2026 20:11:22 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 27 Mar 2026 20:11:22 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 27 Mar 2026 20:11:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 27 Mar 2026 20:11:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 27 Mar 2026 20:11:27 GMT
USER gradle
# Fri, 27 Mar 2026 20:11:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 20:11:29 GMT
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
	-	`sha256:fb82fd334f4b823956c66f78b62e92bf9f1eda8e4ff397c1dda32908a4d666ab`  
		Last Modified: Fri, 27 Mar 2026 19:28:28 GMT  
		Size: 145.5 MB (145459996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfced7944d31e5aca66a9ac303ecaaa4382b9ff4005bd97adff29c4c01fe5ea7`  
		Last Modified: Fri, 27 Mar 2026 19:28:24 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e05c7865d8220f7cf536366eb0855f654708a3944e8f51a86f054b2158a620`  
		Last Modified: Fri, 27 Mar 2026 19:28:24 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca3cb2f52ae826e519222c7b9b943588d3e96574001c3dad4457f68a2923424`  
		Last Modified: Fri, 27 Mar 2026 20:12:04 GMT  
		Size: 1.6 KB (1589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d115cd76e19140012f2d401c5a2bb17cd26014365e838d65cf2f50e823b05ff1`  
		Last Modified: Fri, 27 Mar 2026 20:12:06 GMT  
		Size: 40.5 MB (40513659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9644ad0dc083bc3a9758af1846257e29d1896fb9b7f50da1f4d678584168c9`  
		Last Modified: Fri, 27 Mar 2026 20:12:09 GMT  
		Size: 137.8 MB (137808338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c33907923ef552bbaa78315f203c321d97480fc890d19fb983a6317fcbb59bd`  
		Last Modified: Fri, 27 Mar 2026 20:12:04 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:14cb61d1ec9e72793c223fc4c0d847d7915724528fa743115f4ac68b4b8412aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7042869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3bccc971f4fe89dc80aae1b3c821c7fb0af4574fee7375dfdbbb5ad7cd05bc`

```dockerfile
```

-	Layers:
	-	`sha256:ede19b70a023bf5d71dfdb27e322d128f6bb6f5ed189c55a1f604d5c30705467`  
		Last Modified: Fri, 27 Mar 2026 20:12:05 GMT  
		Size: 7.0 MB (7018346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b36a6f5dd908c2273d5e1f7d5e8c0136468576c1c7cf94fe73edf78b1f0cb65`  
		Last Modified: Fri, 27 Mar 2026 20:12:04 GMT  
		Size: 24.5 KB (24523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:2195a1b68319e72413304996f5c448fbdf06860486e14dc9a7e079bc72196d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386586333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d210a0d3cf9d2bb3ce69791a411ddc79747cbe5a4181f95fd3f30a4e8c0b7c7a`
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
# Fri, 27 Mar 2026 18:59:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Mar 2026 18:59:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:59:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 27 Mar 2026 18:59:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Fri, 27 Mar 2026 18:59:32 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Fri, 27 Mar 2026 18:59:37 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='592a6702b3a07a0e0b82cb38aaab149bfce1b0c24d6b57ddb410bd9009333095';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.18_8.tar.gz';          ;;        ppc64le)          ESUM='5ab89fbde560e1a09386f389dd7881715b896f49c6e9aa974f72d551337dba5e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.18_8.tar.gz';          ;;        s390x)          ESUM='3693469655bcfa2fa5e70907245a2b3bc4236db7d9fa1b9feb0ab7abd235da09';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.18_8.tar.gz';          ;;        x86_64)          ESUM='0c94cbb54325c40dcf026143eb621562017db5525727f2d9131a11250f72c450';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_linux_hotspot_17.0.18_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 27 Mar 2026 18:59:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 27 Mar 2026 18:59:38 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 27 Mar 2026 18:59:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 27 Mar 2026 18:59:38 GMT
CMD ["jshell"]
# Fri, 27 Mar 2026 19:10:23 GMT
CMD ["gradle"]
# Fri, 27 Mar 2026 19:10:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 27 Mar 2026 19:10:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 27 Mar 2026 19:10:23 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 27 Mar 2026 19:10:23 GMT
WORKDIR /home/gradle
# Fri, 27 Mar 2026 19:10:29 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 27 Mar 2026 19:10:29 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 27 Mar 2026 19:10:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 27 Mar 2026 19:10:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 27 Mar 2026 19:10:33 GMT
USER gradle
# Fri, 27 Mar 2026 19:10:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 27 Mar 2026 19:10:34 GMT
USER root
```

-	Layers:
	-	`sha256:9c01cab36040f3f8f1c78284c2d60452730d51f09eb8623c854a44417db02f17`  
		Last Modified: Thu, 26 Mar 2026 18:15:05 GMT  
		Size: 34.4 MB (34434323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92e629fa493b439430775fefb78b6ea7e4f3d723384615f003b8a5913c0ef72`  
		Last Modified: Fri, 27 Mar 2026 19:00:08 GMT  
		Size: 37.8 MB (37835076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf990bea875a90cfb3eb653ef7ea88651ed9063bd030627325ecef3f359339e`  
		Last Modified: Fri, 27 Mar 2026 19:00:09 GMT  
		Size: 135.6 MB (135629137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecea4c23fabccc245ef16395a826101857be3d507ab1e9638a3a20729e27beb`  
		Last Modified: Fri, 27 Mar 2026 19:00:07 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2bb7bdc5a6918b38852e1f8f2e253d0862c8ebb657b8bed981c8abd956bae7`  
		Last Modified: Fri, 27 Mar 2026 19:00:09 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb9ee2e0fffe7e08959ace133a6b6b9ca5c7fa83795caf5380a21ad7ed67fef`  
		Last Modified: Fri, 27 Mar 2026 19:11:02 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5629f994adbd088fc735303e3c032ab55c8dee60b733c0511e780f110ae2b690`  
		Last Modified: Fri, 27 Mar 2026 19:11:03 GMT  
		Size: 40.9 MB (40875049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cf3622484955167080d1248f880804cac348ffdb5d962434fa589ce29083f3`  
		Last Modified: Fri, 27 Mar 2026 19:11:05 GMT  
		Size: 137.8 MB (137808337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d952c5b6cbdb9939105dd4356168c8cf2a28e846d654e7de1dab4a576c2b5d`  
		Last Modified: Fri, 27 Mar 2026 19:11:02 GMT  
		Size: 377.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:9661a5dc1a2966c1c7c09a0bb4bdfbd085d3f9a45c3ceda1e1ea1616d1ff02be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7032024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de16aed4bd1f117b138223329c175827f7e11535460496e3da013808dfd8e1a`

```dockerfile
```

-	Layers:
	-	`sha256:d327fa3f6273da34ea23ce988c92e6b1f2a92b6d968ae462b6688cdb98382918`  
		Last Modified: Fri, 27 Mar 2026 19:11:02 GMT  
		Size: 7.0 MB (7007575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49417c8da10b435b1eab9184a159095b2632c36e60395c950a9431a5b77fdcae`  
		Last Modified: Fri, 27 Mar 2026 19:11:02 GMT  
		Size: 24.4 KB (24449 bytes)  
		MIME: application/vnd.in-toto+json
