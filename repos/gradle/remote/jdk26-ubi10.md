## `gradle:jdk26-ubi10`

```console
$ docker pull gradle@sha256:11851a24a9db0def7c8dbdbb46d7445a058f0e8f1c6cc259a143eeaba284ca8e
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

### `gradle:jdk26-ubi10` - linux; amd64

```console
$ docker pull gradle@sha256:3f296f19fb619a441f59d70b22977dbc4f05e8ef5a5c2a0d20008aeb3649c450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343137079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14dacd922301ce36e9e4eb00fb223a4eee5a07b45c819c2223c538643886e78c`
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
# Wed, 08 Apr 2026 17:27:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:27:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:27:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:27:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:27:42 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 17:27:48 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 08 Apr 2026 17:27:49 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:27:49 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:27:49 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:27:49 GMT
CMD ["jshell"]
# Fri, 10 Apr 2026 16:55:20 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 16:55:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 16:55:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 10 Apr 2026 16:55:20 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 16:55:21 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 16:55:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 10 Apr 2026 16:55:25 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 16:55:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 16:55:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 16:55:27 GMT
USER gradle
# Fri, 10 Apr 2026 16:55:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 16:55:28 GMT
USER root
```

-	Layers:
	-	`sha256:e6c23a286985c06cc6d9b05d3d1e515a2fe5443b2da741ed6bc423f7907d3e67`  
		Last Modified: Thu, 26 Mar 2026 18:05:52 GMT  
		Size: 34.6 MB (34608408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eead742e1b76fa233b87e61d60333071e7bfe3efcaa957b33cf0c2713cdda096`  
		Last Modified: Wed, 08 Apr 2026 17:28:09 GMT  
		Size: 37.5 MB (37455496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29169d65e6097bf63097d7d88f8a8671325f6699d1cf00676bb6a6aed8644254`  
		Last Modified: Wed, 08 Apr 2026 17:28:10 GMT  
		Size: 94.5 MB (94453981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cae758905f208a5642ef3afb3a80b9155bbf57bf26a2397d93f186a866993ff`  
		Last Modified: Wed, 08 Apr 2026 17:28:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73eb171029b9a930705d6d5574e32856b8bf88bfb63ef0f768e089c71cc64448`  
		Last Modified: Wed, 08 Apr 2026 17:28:07 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ca74d85e0690b05144dfeeaf383f6203429a877a7766e5c5ca44b77430460`  
		Last Modified: Fri, 10 Apr 2026 16:55:45 GMT  
		Size: 1.6 KB (1586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422bb34414d989fdcdd951a7511d6c1d4f0cb225f0c60d600abba8950493ed2d`  
		Last Modified: Fri, 10 Apr 2026 16:55:46 GMT  
		Size: 38.8 MB (38781207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e63c61702fed3f5319ce9cf00db165d8e9c818ca54d0f33dd542749082725`  
		Last Modified: Fri, 10 Apr 2026 16:55:50 GMT  
		Size: 137.8 MB (137808336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a02a99050d48162925f15dcca945679bdb8fc10e3abf3a9c88e953344eb98ae`  
		Last Modified: Fri, 10 Apr 2026 16:55:45 GMT  
		Size: 25.6 KB (25615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:939a0fbd6dd4c8e9c5bd5fb45631935c75d1a5e2daf19686fac4f64507822480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275de1b1928f524e9eba3a327a0ff3505745ec7f2df476cb3d3688712df06588`

```dockerfile
```

-	Layers:
	-	`sha256:550b74fc245d1eca9ed2b65b48d92c082ac411bc798ff4761e00146f2510f9aa`  
		Last Modified: Fri, 10 Apr 2026 16:55:45 GMT  
		Size: 7.0 MB (6992432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d35db84aefcbf503e172f16581d5c139dba1a84a777ff717f95438687bc6f4`  
		Last Modified: Fri, 10 Apr 2026 16:55:45 GMT  
		Size: 24.4 KB (24409 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1aef4501cdc80bd3efe70cd3a9f26116e6f130e6f661657644fc85b2b27d4a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339617593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb4a13f126a40f4b9900155f08a8c8d0da7796b906c5171b578db30386c06e1`
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
# Wed, 08 Apr 2026 17:28:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:28:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:28:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:28:18 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:28:18 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 17:28:25 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 08 Apr 2026 17:28:27 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:28:27 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:28:27 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:28:27 GMT
CMD ["jshell"]
# Fri, 10 Apr 2026 16:56:52 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 16:56:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 16:56:52 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 10 Apr 2026 16:56:52 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 16:56:52 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 16:56:56 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 10 Apr 2026 16:56:56 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 16:56:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 16:56:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 16:56:59 GMT
USER gradle
# Fri, 10 Apr 2026 16:56:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 16:56:59 GMT
USER root
```

-	Layers:
	-	`sha256:3bdc97aa816d30cff74675555d7b3f29b652ed3811ef43aff9bf264de81602f2`  
		Last Modified: Thu, 26 Mar 2026 18:05:46 GMT  
		Size: 32.7 MB (32681363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb5ae4959802fc84e97cb06e6f9886b0474432353acc0ad71d2e4a0cab073a`  
		Last Modified: Wed, 08 Apr 2026 17:28:46 GMT  
		Size: 37.4 MB (37405244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619b5ea3cf06f1a78d8e4d8694901cceb4ce15d6781da7dff40908303b5cb19d`  
		Last Modified: Wed, 08 Apr 2026 17:28:47 GMT  
		Size: 93.4 MB (93395896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e21b71c200a1105fffcb0f7bac5e81347b2bd87d34505a0d0542da28974916`  
		Last Modified: Wed, 08 Apr 2026 17:28:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4881aae75613fb521c82651cef4a01e0fbdf133792014bb201cbb79528c00aa7`  
		Last Modified: Wed, 08 Apr 2026 17:28:44 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adff2e73dab67d50c7196a9b82eb402c066bc548306e385513d305584e2860a`  
		Last Modified: Fri, 10 Apr 2026 16:57:17 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff919224a097a0bd5e2afb2902793eb3e0cba38501fe5fba7226d4d76f32678`  
		Last Modified: Fri, 10 Apr 2026 16:57:19 GMT  
		Size: 38.3 MB (38293385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4c02042b6b2d838e32c72215d31302a701d422838649c73a8d0624601a3d8c`  
		Last Modified: Fri, 10 Apr 2026 16:57:21 GMT  
		Size: 137.8 MB (137808334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b19c49173812d204931fdc654f783c54f14e2ad794f1163b566346c407202b9`  
		Last Modified: Fri, 10 Apr 2026 16:57:17 GMT  
		Size: 29.3 KB (29338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:3342ee55adc98cce7675a9fcfc0c5a6dde1f39e1090606bd5580a09a58fd72d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1673651ed15a2adacf9676b5dd80017c1b23c8cfdbab490a11998cf55c3c1e`

```dockerfile
```

-	Layers:
	-	`sha256:ce82764f7bc131fadb0ed9058a3ae809bb4c1f41727ffd9b6c8dbdb3a999b766`  
		Last Modified: Fri, 10 Apr 2026 16:57:18 GMT  
		Size: 7.0 MB (6990685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1d0dc2a1319994355ca2dccf01ef4986b4de5051bfe187cd9e2cea5c1d6342`  
		Last Modified: Fri, 10 Apr 2026 16:57:17 GMT  
		Size: 24.6 KB (24606 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; ppc64le

```console
$ docker pull gradle@sha256:133579ac01031d392508a4b78f8c313a03a9f3f7e5856940d2a4dbcfef6a429f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (350044980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057210c894126bde3c9c7ee4abb758572d1d0bc5ed35d556c6bd6390e30cc138`
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
# Wed, 08 Apr 2026 17:37:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:37:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:37:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:37:31 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:37:31 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 17:37:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 08 Apr 2026 17:37:42 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:37:42 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:37:42 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:37:42 GMT
CMD ["jshell"]
# Fri, 10 Apr 2026 16:55:47 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 16:55:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 16:55:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 10 Apr 2026 16:55:47 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 16:55:47 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 16:56:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 10 Apr 2026 16:56:16 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 16:56:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 16:56:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 16:56:20 GMT
USER gradle
# Fri, 10 Apr 2026 16:56:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 16:56:22 GMT
USER root
```

-	Layers:
	-	`sha256:d3afc82808d99ce4baa1bde62af82befcf71b8d6cb81303429e8a1936966a71f`  
		Last Modified: Thu, 26 Mar 2026 18:15:14 GMT  
		Size: 38.7 MB (38703412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6309f5aeaaea98b26ab4eaad66da90b6f28839e50e4697eaec9061103b360a44`  
		Last Modified: Wed, 08 Apr 2026 17:38:27 GMT  
		Size: 39.2 MB (39215178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df497e6745d7c141570880857faace1cd301ccaec1ce89ec487681b4d5522b34`  
		Last Modified: Wed, 08 Apr 2026 17:38:29 GMT  
		Size: 93.8 MB (93782985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711465d19f9686195f44c71e42a29c9da166e84075d714184b740d31b0f67264`  
		Last Modified: Wed, 08 Apr 2026 17:38:23 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590d071effc60968526892eb91af310c8f1a77aec364abcdc4babdf55471e69a`  
		Last Modified: Wed, 08 Apr 2026 17:38:23 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93d0cf454fe500775cc782f98710ffc615a57898015da1c70c9d0b3dd75abc9`  
		Last Modified: Fri, 10 Apr 2026 16:57:12 GMT  
		Size: 1.6 KB (1593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2277e589e20ee8098e616d4e2992e126b1f686efff2c54abefac728253d7ccd`  
		Last Modified: Fri, 10 Apr 2026 16:57:14 GMT  
		Size: 40.5 MB (40530644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148385f81073b60e1acd484c50ebccd8bbd18a4fa716e639eece43437e84c274`  
		Last Modified: Fri, 10 Apr 2026 16:57:16 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326a2aae7a425835dbc6418d0d942d8900268d2ef812f49733230b6450c17502`  
		Last Modified: Fri, 10 Apr 2026 16:57:12 GMT  
		Size: 379.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:b29ce8a26cba435607e9537d9b228ea814064a36c01ea2674003f8ece3cce749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6992267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28761b729901fd9d9677e9bd0362295f2df8823fc005f6d29f58efd8d2134877`

```dockerfile
```

-	Layers:
	-	`sha256:b50e9caacd988c31f51b67901a9baaea4fd54046266182dc6e569121a76d909b`  
		Last Modified: Fri, 10 Apr 2026 16:57:12 GMT  
		Size: 7.0 MB (6967786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8acb389f3177404ea65994c7c3a513aa875b6e9c028f3db3f132aa1a995d88e`  
		Last Modified: Fri, 10 Apr 2026 16:57:11 GMT  
		Size: 24.5 KB (24481 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-ubi10` - linux; s390x

```console
$ docker pull gradle@sha256:55fd0c21b09d901315b93f7c5b9bd441177e23d0142f72bf6001631d6d2034c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.5 MB (341513424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53575b79f26d2a44b7a94e61f7f0cc07f14dd23fa40ea03c153db07f12f5e992`
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
# Wed, 08 Apr 2026 17:23:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 08 Apr 2026 17:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Apr 2026 17:23:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 08 Apr 2026 17:23:10 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 08 Apr 2026 17:23:10 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 08 Apr 2026 17:23:15 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='e8ff1f23c5acef74d1b4937dadd67286d67be06758f5d9dca5478c35bf404e83';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_aarch64_linux_hotspot_26_35.tar.gz';          ;;        ppc64le)          ESUM='7396fc32c311429c4b1573ebfc98eca6b82c2735f9f0e23acbccdcb43e0edee9';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_ppc64le_linux_hotspot_26_35.tar.gz';          ;;        s390x)          ESUM='87fcdbbfd0adfd458922d8f8019eda23755aba597e386de2397f84cdf1b58808';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_s390x_linux_hotspot_26_35.tar.gz';          ;;        x86_64)          ESUM='68e19ba53b7f1f74635c13f809e5db36cebccf3ae9e752423dd92d2ad7d831ef';          BINARY_URL='https://github.com/adoptium/temurin26-binaries/releases/download/jdk-26%2B35/OpenJDK26U-jdk_x64_linux_hotspot_26_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 08 Apr 2026 17:23:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 08 Apr 2026 17:23:17 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 08 Apr 2026 17:23:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 08 Apr 2026 17:23:17 GMT
CMD ["jshell"]
# Fri, 10 Apr 2026 17:19:50 GMT
CMD ["gradle"]
# Fri, 10 Apr 2026 17:19:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 10 Apr 2026 17:19:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 10 Apr 2026 17:19:50 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 10 Apr 2026 17:19:50 GMT
WORKDIR /home/gradle
# Fri, 10 Apr 2026 17:20:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 10 Apr 2026 17:20:05 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 10 Apr 2026 17:20:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 10 Apr 2026 17:20:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 10 Apr 2026 17:20:09 GMT
USER gradle
# Fri, 10 Apr 2026 17:20:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 10 Apr 2026 17:20:10 GMT
USER root
```

-	Layers:
	-	`sha256:9c01cab36040f3f8f1c78284c2d60452730d51f09eb8623c854a44417db02f17`  
		Last Modified: Thu, 26 Mar 2026 18:15:05 GMT  
		Size: 34.4 MB (34434323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde87df0de0c9388c443305e699793fefd66d7bc5663da7b0d9334bf656ed497`  
		Last Modified: Wed, 08 Apr 2026 17:23:53 GMT  
		Size: 37.8 MB (37835564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba4856bc46c50f98ecda2074068782a2a953000c3ab5da511223dacd4949deb`  
		Last Modified: Wed, 08 Apr 2026 17:23:55 GMT  
		Size: 90.5 MB (90548299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00ae403ba25a3b595bb7484eff779a17eb509a55768ecd5d8636cc0ca283611`  
		Last Modified: Wed, 08 Apr 2026 17:23:52 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f4f4bdc26c0fd7ec0a10564cc249730f96875415b067ce768a7b4f25b6829d`  
		Last Modified: Wed, 08 Apr 2026 17:23:52 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ac2584cff42f878df7c2a6e892daba45a50b0ddf0e5b73a8067f01e3c292e0`  
		Last Modified: Fri, 10 Apr 2026 17:20:37 GMT  
		Size: 1.6 KB (1587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4081361f705adf744897de2ac78c0b095fb9f018cf86dc1a19e96277a895aa`  
		Last Modified: Fri, 10 Apr 2026 17:20:39 GMT  
		Size: 40.9 MB (40882486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c380931fb0a4e4ab5857d05b4f0bf62704991e409391091ea514e793073a91f7`  
		Last Modified: Fri, 10 Apr 2026 17:20:41 GMT  
		Size: 137.8 MB (137808338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d624421c3a477887591716080eec5426b71ed113e55eb6fd2fc219fab079d47`  
		Last Modified: Fri, 10 Apr 2026 17:20:38 GMT  
		Size: 376.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-ubi10` - unknown; unknown

```console
$ docker pull gradle@sha256:aaa0af3a11bf7b85394398d6b3f6e755a1f9aa1be17b7946371421c0b37d6f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6982672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df77576625a5d80d367d21e73403dfdace7963d1478c97c131e6912806ae5b2a`

```dockerfile
```

-	Layers:
	-	`sha256:917dded95934004a4b09a219d50326742b9c9538832f8e4e9c4f73d6c1ef2e68`  
		Last Modified: Fri, 10 Apr 2026 17:20:38 GMT  
		Size: 7.0 MB (6958265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3740814bd03ff7ade5442885915ff8de646f8cb50869eff53be3a393ab077073`  
		Last Modified: Fri, 10 Apr 2026 17:20:37 GMT  
		Size: 24.4 KB (24407 bytes)  
		MIME: application/vnd.in-toto+json
