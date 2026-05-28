## `gradle:9-jdk21-ubi`

```console
$ docker pull gradle@sha256:e552f4f4effcce08e712956de395c2721e54bfcd353ac30782fa7efdbb0af9bc
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

### `gradle:9-jdk21-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:590b8cb9cff1fe7616d61169e1495fe1c01ad95c22afcb46b1b22029ac2667d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410933600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cfa493bc0b61148b00605ea0af00cf01b93ea578f343011c0d244fa3ef60b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 27 May 2026 06:12:12 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:12:12 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:12:12 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:12:12 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:12:12 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:12:12 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:12:12 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:12:12 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:12:12 GMT
ENV container oci
# Wed, 27 May 2026 06:12:12 GMT
COPY dir:8cc023cf96d9d3899063545e0c3b25ee410727bc8ef5903cc1b3e3e22d98dc1f in /      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:12:13 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:12:13 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:919ce0635818e127299907aac3d5ec8b04328702d69e0d804c99d87a631c2e20 in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:12:13 GMT
COPY file:919ce0635818e127299907aac3d5ec8b04328702d69e0d804c99d87a631c2e20 in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:12:13 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:11:58Z" "org.opencontainers.image.created"="2026-05-27T06:11:58Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:11:58Z
# Wed, 27 May 2026 22:37:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:37:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:37:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:37:20 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:37:20 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 27 May 2026 22:37:27 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:37:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:37:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:37:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:37:28 GMT
CMD ["jshell"]
# Wed, 27 May 2026 23:11:43 GMT
CMD ["gradle"]
# Wed, 27 May 2026 23:11:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 23:11:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 23:11:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 23:11:43 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 23:11:47 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 23:11:47 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 23:11:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 23:11:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 23:11:49 GMT
USER gradle
# Wed, 27 May 2026 23:11:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 23:11:50 GMT
USER root
```

-	Layers:
	-	`sha256:8b457fb1b26320aa35da6d429ea0efa5a81d9f904a24a8d0a4e1a1efcfd0e7b8`  
		Last Modified: Wed, 27 May 2026 07:33:17 GMT  
		Size: 34.9 MB (34902395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4388b8624524602d05952be02a0130f99ee994082bada674d1a753650cdb49`  
		Last Modified: Wed, 27 May 2026 22:37:48 GMT  
		Size: 37.7 MB (37749799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cfe212629b52054a95fca509000c57be8e5e060d56f32eaa37327e3c84b2f6`  
		Last Modified: Wed, 27 May 2026 22:37:51 GMT  
		Size: 158.2 MB (158172699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a7381c9be19ff2b8b026307de53a4a3b5cae8b566050cef45853f76fd1c75a`  
		Last Modified: Wed, 27 May 2026 22:37:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a206aa3812d97ee8323c48268b57b0c6f45dbd2154f829d0814fec9cfc41e029`  
		Last Modified: Wed, 27 May 2026 22:37:46 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03603c91b1203eea5c4542843f08f799cac08d4be0bc85cdb424597fc8200b55`  
		Last Modified: Wed, 27 May 2026 23:12:09 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65c69c582ac393bb4700ad58a70d8235a834331c58c4eb3d75df9eba4936ead`  
		Last Modified: Wed, 27 May 2026 23:12:11 GMT  
		Size: 39.8 MB (39842074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9266f34e4a6fcfa54d8fd6655e08ddc69e6f36991db5c64da31bcedbc194748d`  
		Last Modified: Wed, 27 May 2026 23:12:13 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca8b9eb07cdc82e775eb020f575b0c655fc9e84d62dc49b2deb80acfd090b7e`  
		Last Modified: Wed, 27 May 2026 23:12:09 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:6929f5b530da77274cf668d21b7069f5286874ff2dee2942c86061ccf04932d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7103035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5cefddae4be4ab88d25de63ffea4beaffa5df6eb6969bb30d05e5c1382884c`

```dockerfile
```

-	Layers:
	-	`sha256:f4ad744d2fb8fced6326652ccfa0217f9eb04c7332f08824e965097561ddc14b`  
		Last Modified: Wed, 27 May 2026 23:12:09 GMT  
		Size: 7.1 MB (7078580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272eea50d2017b390d48012f06ff87b36dd19a732dc473e1ba8647d71b57017a`  
		Last Modified: Wed, 27 May 2026 23:12:08 GMT  
		Size: 24.5 KB (24455 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0964483d3b5d4e3ec3cdaf73260dfeba8cd03bacccc553d30b5ac02c8d82f351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.8 MB (406775498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dedcd06f7cecf64195c196f446df6963072224f37c0dd155b040f344e3cbda`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 27 May 2026 06:14:32 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:14:32 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:14:32 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:14:32 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:14:32 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:14:32 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:14:32 GMT
ENV container oci
# Wed, 27 May 2026 06:14:33 GMT
COPY dir:144798cc4c14efe6d25c10c7a6f149af1045784afd86a94e99d04f534f9bbb05 in /      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:14:33 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:14:33 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
COPY file:83615dc098d46f372c6688f68025f354351bfbb3ed132d56c889042d90463ecf in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:14:34 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:14:17Z" "org.opencontainers.image.created"="2026-05-27T06:14:17Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:14:17Z
# Wed, 27 May 2026 22:37:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:37:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:37:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:37:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:37:37 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 27 May 2026 22:37:44 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:37:45 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:37:45 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:37:45 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:37:45 GMT
CMD ["jshell"]
# Wed, 27 May 2026 23:11:00 GMT
CMD ["gradle"]
# Wed, 27 May 2026 23:11:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 23:11:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 23:11:00 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 23:11:00 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 23:11:03 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 23:11:03 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 23:11:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 23:11:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 23:11:06 GMT
USER gradle
# Wed, 27 May 2026 23:11:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 23:11:07 GMT
USER root
```

-	Layers:
	-	`sha256:94a14999202bc800f78441edfa1b48a3f6b5a799655652a41a4ef92004acb9c3`  
		Last Modified: Wed, 27 May 2026 07:33:15 GMT  
		Size: 33.1 MB (33062079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d1fa975ce3866da18a22628155a583f5a5fc9e32c7e07a1a4af941ae713200`  
		Last Modified: Wed, 27 May 2026 22:38:05 GMT  
		Size: 37.7 MB (37681226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436af8d7ca89c65c8f929843869799df169835329e2fab087cd14762a927f40e`  
		Last Modified: Wed, 27 May 2026 22:38:08 GMT  
		Size: 156.5 MB (156464390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95c1638553cc6298c0113290ce8432b80fe389d8e3c34da01bfbf524a6f2aa7`  
		Last Modified: Wed, 27 May 2026 22:38:03 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5494ed118b1939f96c6317e15b410101f18f9fbabca555b5ee8734f4c7b46e`  
		Last Modified: Wed, 27 May 2026 22:38:04 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f90f15eaa2be696075e5b197a693197b62d4731af02731c92ccba17c63844`  
		Last Modified: Wed, 27 May 2026 23:11:26 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc956cc46d73ccae60a56ddeaa7264165ceeb74c1abd050296e05aa5a1526617`  
		Last Modified: Wed, 27 May 2026 23:11:28 GMT  
		Size: 39.3 MB (39297453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8657938a7f0795cbee630d9d92b32e9ce9003baecc31235786a7e12a51db884`  
		Last Modified: Wed, 27 May 2026 23:11:30 GMT  
		Size: 140.2 MB (140236982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdcc41b3f823515d86e909bdf6f7dd928396873bc3a967bb9b69bc1bafd5a44`  
		Last Modified: Wed, 27 May 2026 23:11:26 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:1aceaa63502ef7460865897848bbdcf8091d446c99c40fb5ca104a4812d4ac8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7101487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03d7e35bc9b11a52688f09762d3fb243748d8147004603868eda4690abd6ab3`

```dockerfile
```

-	Layers:
	-	`sha256:f0936f77671759fe10ebd46487a626ba175065011360ebfb2e0a3622c4ed7e9f`  
		Last Modified: Wed, 27 May 2026 23:11:26 GMT  
		Size: 7.1 MB (7076836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e2eee975f97c1edfb1eab8268514a4dc35f359d3aa5e28c0509c9a5d970bcf6`  
		Last Modified: Wed, 27 May 2026 23:11:26 GMT  
		Size: 24.7 KB (24651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:b6e8df6c0db41efb78d9d568818d4ca6bfca39e1fff3ba40b5d7542fa6f567e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.7 MB (418715921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9109d9c786cbb8a021c6ee359a60707cb9a03145b0cb857974164f157e8e5e82`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 27 May 2026 06:14:57 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:14:57 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:14:58 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:14:58 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:14:58 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:14:58 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:14:58 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:58 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:14:59 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:14:59 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:14:59 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:15:00 GMT
ENV container oci
# Wed, 27 May 2026 06:15:05 GMT
COPY dir:3c79ef63a7976ed53bc357ee61420f17b1c4d01f16daa9a157b46e996d5ae20c in /      
# Wed, 27 May 2026 06:15:06 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:15:06 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:15:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:15:07 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:15:08 GMT
COPY file:5604aea5cf04212fca8939538465f845888885b3e8d5cba8ef672e5a589974b7 in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:15:10 GMT
COPY file:5604aea5cf04212fca8939538465f845888885b3e8d5cba8ef672e5a589974b7 in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:15:11 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:13:56Z" "org.opencontainers.image.created"="2026-05-27T06:13:56Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:13:56Z
# Wed, 27 May 2026 22:50:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:50:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:50:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:50:47 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:50:47 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 27 May 2026 22:53:43 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:53:47 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:53:48 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:53:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:53:48 GMT
CMD ["jshell"]
# Wed, 27 May 2026 23:09:29 GMT
CMD ["gradle"]
# Wed, 27 May 2026 23:09:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 23:09:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 23:09:29 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 23:09:29 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 23:09:53 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 23:09:53 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 23:09:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 23:09:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 23:09:58 GMT
USER gradle
# Wed, 27 May 2026 23:09:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 23:09:59 GMT
USER root
```

-	Layers:
	-	`sha256:d339a2f2276a8d859309603363be4a2e3264f8a5a443e066c45ef5518856d381`  
		Last Modified: Wed, 27 May 2026 10:57:44 GMT  
		Size: 39.0 MB (39023856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58939e04772041c6139b9c72eb21d342c8fe4b6f1a4fe1a247ee089431c487cc`  
		Last Modified: Wed, 27 May 2026 22:51:27 GMT  
		Size: 39.5 MB (39503510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431979a8373c81060e064acc7468cae0b5ad0966b7fd7a8813230e5ca1e20d2d`  
		Last Modified: Wed, 27 May 2026 22:54:26 GMT  
		Size: 158.3 MB (158348525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633259eeaec8618d3139e6636b92980be8db6a89418aef00425a8ccd66bcfda7`  
		Last Modified: Wed, 27 May 2026 22:54:22 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5a2ade78297a8276c7d342e63e71ee879d196abc947929c6a573a859513744`  
		Last Modified: Wed, 27 May 2026 22:54:23 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698ceba8280e602bbba9ce325c7c653eeb598e17db965b566c2ef22b1e376efb`  
		Last Modified: Wed, 27 May 2026 23:10:43 GMT  
		Size: 1.6 KB (1589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411caf62fd0b18ccb4ec9379b892fb83647f47c9159fed8ba2bd63012902935c`  
		Last Modified: Wed, 27 May 2026 23:10:45 GMT  
		Size: 41.6 MB (41598626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581d84133aa2834132b0d779b84fb7cf95149e8b37aa55026fd76c597d3ec0d7`  
		Last Modified: Wed, 27 May 2026 23:10:48 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d2011aba9fbfbc722fdc75a6c13dda50982d10fee735c67e51e0e9a05a1a58`  
		Last Modified: Wed, 27 May 2026 23:10:43 GMT  
		Size: 378.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:57ec4ba6ef861e9b071c850240c54c290e972593cb6681ec36e8ccc60b09d61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7094525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e79f00420c78f5db5b30210dad095c856fba79c3f882dbb6fd34fb0e6b7c87`

```dockerfile
```

-	Layers:
	-	`sha256:7862745fe1a5656f8991ab7c3edf36432112103afddd1bdc7130ea5b9e4cf389`  
		Last Modified: Wed, 27 May 2026 23:10:43 GMT  
		Size: 7.1 MB (7069998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492d236fe8e1b3401e1036518979b09f8d88ec34689711516a3c92861c5ea583`  
		Last Modified: Wed, 27 May 2026 23:10:43 GMT  
		Size: 24.5 KB (24527 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:9acb4aac76f87551c5844ab1db5ea43ba6a522c04de793472c78a8fd34e573f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 MB (402389179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6b5b12c67fd74fed4af8e3564a87863565b5ad089e5c8ea68aec39800ea3d9`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 27 May 2026 06:37:00 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 27 May 2026 06:37:00 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 27 May 2026 06:37:00 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 27 May 2026 06:37:00 GMT
LABEL com.redhat.component="ubi10-minimal-container"       name="ubi10/ubi-minimal"       version="10.2"       cpe="cpe:/o:redhat:enterprise_linux:10.2"       distribution-scope="public"
# Wed, 27 May 2026 06:37:00 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 27 May 2026 06:37:00 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 10."
# Wed, 27 May 2026 06:37:00 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 10 Minimal"
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.openshift.expose-services=""
# Wed, 27 May 2026 06:37:00 GMT
LABEL io.openshift.tags="minimal rhel10"
# Wed, 27 May 2026 06:37:00 GMT
ENV container oci
# Wed, 27 May 2026 06:37:01 GMT
COPY dir:24d1f0c37ae2ecf8290e1663d221246314d1b68d602e33735e6d32665445372e in /      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:5de33b5fc08b00635bccf9134a18978dba13e2250aa51838f9969515a3957847 in /etc/yum.repos.d/.      
# Wed, 27 May 2026 06:37:01 GMT
CMD ["/bin/bash"]
# Wed, 27 May 2026 06:37:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /usr/share/buildinfo/content-sets.json      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:595171150af68abc798ea385f7988d74b566aa8e84babff137f00b08b2164683 in /root/buildinfo/content_manifests/content-sets.json      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:4188614bc7118984387709b86ec90ee5a895ba0f9b561a8cf875fcae15cc3f1f in /usr/share/buildinfo/labels.json      
# Wed, 27 May 2026 06:37:01 GMT
COPY file:4188614bc7118984387709b86ec90ee5a895ba0f9b561a8cf875fcae15cc3f1f in /root/buildinfo/labels.json      
# Wed, 27 May 2026 06:37:01 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "org.opencontainers.image.revision"="3aa29655e860e8f28ee9014c3803f132b3b1e65d" "build-date"="2026-05-27T06:36:19Z" "org.opencontainers.image.created"="2026-05-27T06:36:19Z" "release"="1779862102"org.opencontainers.image.revision=3aa29655e860e8f28ee9014c3803f132b3b1e65d,org.opencontainers.image.created=2026-05-27T06:36:19Z
# Wed, 27 May 2026 22:39:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 27 May 2026 22:39:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 22:39:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 May 2026 22:39:28 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en         gnupg2     ;     microdnf clean all # buildkit
# Wed, 27 May 2026 22:39:28 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Wed, 27 May 2026 22:40:14 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='8d498ec88e1c1989fab95c6784240ab92d011e29c54d20a3f9c324b13476f9ad';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.11_10.tar.gz';          ;;        ppc64le)          ESUM='3d043ae96d2343962bf2307d8c55f19849fbfa4c6be9fe164a77d79263f0d989';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.11_10.tar.gz';          ;;        s390x)          ESUM='14dbe3cb226e64b945a36bea32686e8deec746504fe3ccee8de585c54af41ffd';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_s390x_linux_hotspot_21.0.11_10.tar.gz';          ;;        x86_64)          ESUM='4b2220e232a97997b436ca6ab15cbf70171ecff52958a46159dfa5a8c44ca4de';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.11%2B10/OpenJDK21U-jdk_x64_linux_hotspot_21.0.11_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Wed, 27 May 2026 22:40:16 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 27 May 2026 22:40:16 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 27 May 2026 22:40:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 27 May 2026 22:40:16 GMT
CMD ["jshell"]
# Wed, 27 May 2026 23:09:44 GMT
CMD ["gradle"]
# Wed, 27 May 2026 23:09:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 27 May 2026 23:09:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 27 May 2026 23:09:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 27 May 2026 23:09:44 GMT
WORKDIR /home/gradle
# Wed, 27 May 2026 23:09:51 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make         curl-minimal         wget         tar                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Wed, 27 May 2026 23:09:51 GMT
ENV GRADLE_VERSION=9.5.1
# Wed, 27 May 2026 23:09:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Wed, 27 May 2026 23:09:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 27 May 2026 23:09:58 GMT
USER gradle
# Wed, 27 May 2026 23:09:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 27 May 2026 23:09:58 GMT
USER root
```

-	Layers:
	-	`sha256:5e0d999553a87b2b92e291dab9ef17c167202f1dbb15b260d71e176269309f5d`  
		Last Modified: Wed, 27 May 2026 10:57:27 GMT  
		Size: 34.7 MB (34680084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f791d9d2e9057d9aa1ff0de899ae842378191648f3f54117e24f972cf721e84`  
		Last Modified: Wed, 27 May 2026 22:39:52 GMT  
		Size: 38.1 MB (38119066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708c1fef362f54ff5788487378ff6f78d4353a759430f1ea83a10daa9e761201`  
		Last Modified: Wed, 27 May 2026 22:40:44 GMT  
		Size: 147.4 MB (147390197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d1e3907804c8a69b532970b4aaae94183061ddf07ed28756706389aaf4ac91`  
		Last Modified: Wed, 27 May 2026 22:40:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907dec967ae31a025efe5886afc2a014d5c2e8e3abc219d9c243033e4c4f6342`  
		Last Modified: Wed, 27 May 2026 22:40:41 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c98d3c9fe947e371637b6550d1a5b15a427bfcc3cf43a971fa87c38341067d`  
		Last Modified: Wed, 27 May 2026 23:10:29 GMT  
		Size: 1.6 KB (1583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf795fc2166f887050a55e590f9c49dcf6147e6bd9a239d0a853e8920d6841`  
		Last Modified: Wed, 27 May 2026 23:10:32 GMT  
		Size: 42.0 MB (41958435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96db85be0a3c1618fc77fa2daebb93f56564e886b31e66caf3fc42d4b0e6bee`  
		Last Modified: Wed, 27 May 2026 23:10:34 GMT  
		Size: 140.2 MB (140236988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098224e99ebde4681332a91a211c39ac7fa892e778571a3b7099643c5168f91b`  
		Last Modified: Wed, 27 May 2026 23:10:30 GMT  
		Size: 374.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:6c3a2c67759f788f622ae662fd513e03cd50b2075a64a3bdf2645a7b81edbcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7083680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d317b20df6010875a87e350cad9c371ff55e498657b87f47cc8ce3023ebf6950`

```dockerfile
```

-	Layers:
	-	`sha256:a87144066818e1834cdae90ae877cececba20ca21b38941859e1e4baf4221023`  
		Last Modified: Wed, 27 May 2026 23:10:30 GMT  
		Size: 7.1 MB (7059227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c03e8a04ee05e9ee784048a393c6a05e35c0181c90852afab0bb2c6e81f2937`  
		Last Modified: Wed, 27 May 2026 23:10:30 GMT  
		Size: 24.5 KB (24453 bytes)  
		MIME: application/vnd.in-toto+json
