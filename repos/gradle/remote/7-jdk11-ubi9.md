## `gradle:7-jdk11-ubi9`

```console
$ docker pull gradle@sha256:8127baefac322e94e80ac01fecf7e7285e33fe9ec86f7c25a9bde612b8e5cd14
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

### `gradle:7-jdk11-ubi9` - linux; amd64

```console
$ docker pull gradle@sha256:2f131a0573649238b13228e08ba8ffa76405c81d51a6ee0367e6d3c38aba424b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.1 MB (377137204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943d8b9be21fc16e98e2b7f5b13b90b6e435a02166bc4659fafae96eaa1e1e66`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:14 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:14 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:14 GMT
COPY dir:37b1ea11a739ebaa3fdc4f74d963b56e5e50e2e4b048d008948978527dfc6171 in /      
# Mon, 15 Jun 2026 04:14:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:14 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
COPY file:df404a029d790f68220d23dfb53723434fcb08b3371b285cdfe02b423b1e978d in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:15 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:02Z" "org.opencontainers.image.created"="2026-06-15T04:14:02Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:02Z
# Mon, 15 Jun 2026 23:13:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:52 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:52 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Mon, 15 Jun 2026 23:13:58 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:14:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:14:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:14:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:14:00 GMT
CMD ["jshell"]
# Mon, 15 Jun 2026 23:34:13 GMT
CMD ["gradle"]
# Mon, 15 Jun 2026 23:34:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 15 Jun 2026 23:34:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 15 Jun 2026 23:34:13 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 15 Jun 2026 23:34:13 GMT
WORKDIR /home/gradle
# Mon, 15 Jun 2026 23:34:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 15 Jun 2026 23:34:16 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 15 Jun 2026 23:34:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 15 Jun 2026 23:34:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:34:19 GMT
USER gradle
# Mon, 15 Jun 2026 23:34:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 15 Jun 2026 23:34:19 GMT
USER root
```

-	Layers:
	-	`sha256:48538841ca5147d36a25e82713e079413d3c2a137f5ea5df68a1c5da1e3a677e`  
		Last Modified: Mon, 15 Jun 2026 04:45:40 GMT  
		Size: 40.7 MB (40680192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8c7b76e6f0b6ac8c7260c87a0e7e67d188a1f6151793ed8427ebed192bdf36`  
		Last Modified: Mon, 15 Jun 2026 23:14:16 GMT  
		Size: 27.7 MB (27664144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f8ac8c400b3f9810471581974ffc6f775d89f3f403cbe2d7a5c9e9adfab26a`  
		Last Modified: Mon, 15 Jun 2026 23:14:19 GMT  
		Size: 142.3 MB (142348788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d434ef7dbe56a89519f5fd106c281676c742a5a834c16bd5b2ada15df92ddaf0`  
		Last Modified: Mon, 15 Jun 2026 23:14:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5317b0071b6f24cada9f7d443a94dcefad92a18b5bb38bfef0c882ab00d904`  
		Last Modified: Mon, 15 Jun 2026 23:14:15 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a91d4b9336eb399b684a3d2a3249aa7cb7b52b529d2ee6eeb4db34f1498721`  
		Last Modified: Mon, 15 Jun 2026 23:34:36 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73768b7a29c5eecd08bbf3787abc228b00f3771d51a5e53b55b304408e9fc15`  
		Last Modified: Mon, 15 Jun 2026 23:34:37 GMT  
		Size: 37.9 MB (37915598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee3e6a7375e34a4aefe8151ae4edb411f99fe9f8f64308fdefcb6c8a8208fe9`  
		Last Modified: Mon, 15 Jun 2026 23:34:40 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2601b31c972fd8526b56117527030e9322cf7dc94076fada245b8a13c232fbb`  
		Last Modified: Mon, 15 Jun 2026 23:34:36 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:6b9f0e459cc72e8737988bba9b071aa5db2c02a4ceff81027fa2ffafabaf5d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a939d41019542ea3f0246d1f8cf6b475a91e983107163f4bdc9f76c93633c1`

```dockerfile
```

-	Layers:
	-	`sha256:e4a14bb1600f398daf8234493693851ee07706154433adaf8f01d5c93901a901`  
		Last Modified: Mon, 15 Jun 2026 23:34:36 GMT  
		Size: 5.3 MB (5336598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630312d50fcaadcd53d3471b01e2c93efe7b76ab923f55f834622028414043d7`  
		Last Modified: Mon, 15 Jun 2026 23:34:36 GMT  
		Size: 23.5 KB (23547 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4f152e6a43e8ee62e6a85b04fa66df28eab54426b097166312eb7abae0f40091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.8 MB (371752549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51cd6df37acf2a08b8489cd6a2274d25908f8dd7646cc2559dcd5921f52fd8de`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:15:43 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:15:43 GMT
ENV container oci
# Mon, 15 Jun 2026 04:15:44 GMT
COPY dir:553346a2ec24f0a482095311bcf74fe382a66c8cb976ea0b61f6d55ee917aca4 in /      
# Mon, 15 Jun 2026 04:15:44 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:15:44 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
COPY file:f3a7d39ee1404b5d93b5454e6014ed02f219e8a196f3df41d84d2e0e61c935f5 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:15:45 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:15:31Z" "org.opencontainers.image.created"="2026-06-15T04:15:31Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:15:31Z
# Mon, 15 Jun 2026 23:13:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:13:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:13:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:13:24 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:13:24 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Mon, 15 Jun 2026 23:13:32 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:13:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:13:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:13:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:13:33 GMT
CMD ["jshell"]
# Mon, 15 Jun 2026 23:26:45 GMT
CMD ["gradle"]
# Mon, 15 Jun 2026 23:26:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 15 Jun 2026 23:26:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 15 Jun 2026 23:26:45 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 15 Jun 2026 23:26:45 GMT
WORKDIR /home/gradle
# Mon, 15 Jun 2026 23:26:48 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Mon, 15 Jun 2026 23:26:48 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 15 Jun 2026 23:26:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 15 Jun 2026 23:26:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 15 Jun 2026 23:26:51 GMT
USER gradle
# Mon, 15 Jun 2026 23:26:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 15 Jun 2026 23:26:51 GMT
USER root
```

-	Layers:
	-	`sha256:06005d885e6ce6c0708c4294316153d2de40b8859a131bbba11795c4f1e5eb71`  
		Last Modified: Mon, 15 Jun 2026 04:58:33 GMT  
		Size: 38.9 MB (38873024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaca93ade8903a8857aaadc68625da248ab5601cb5a874f2f61bdcab97c0305`  
		Last Modified: Mon, 15 Jun 2026 23:13:50 GMT  
		Size: 28.1 MB (28098987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a782c1ab3493b863637be4cc8cd56bd64e08e46c52b94d0b923d083dbb144dec`  
		Last Modified: Mon, 15 Jun 2026 23:13:52 GMT  
		Size: 139.0 MB (139040687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f364209f45709a092ae3f948c484ed306f2eb51569c1c94121b27b845935d5d`  
		Last Modified: Mon, 15 Jun 2026 23:13:48 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28af555b57197f834bc9bce1e6cbee5b9a874c5596124132de4599f5a415ff86`  
		Last Modified: Mon, 15 Jun 2026 23:13:48 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d9bd9e51356f7187329d8649e61d94b040923a461e4d418397011278e2e2f7`  
		Last Modified: Mon, 15 Jun 2026 23:27:06 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad510d1e3a38e6103a9c3dba57852eb32dd0d2f5ceb1f362a32a405d56c8c6c`  
		Last Modified: Mon, 15 Jun 2026 23:27:08 GMT  
		Size: 37.2 MB (37206745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e46ae0732231b259788776b60bb012fcd0fd3c6ae9c5670770240b75836baa9`  
		Last Modified: Mon, 15 Jun 2026 23:27:10 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715496d0cbf3b6c3ce19b2e23a4ca3fbc634172b67ce6f893c31df44edcc7204`  
		Last Modified: Mon, 15 Jun 2026 23:27:07 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:d93a44d56c52edb89c9632b3b578f1112c7dd6b177422672575971dd8ca01ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15973f8a2e391c119290c0619bed65c4365da7cf30298092bb551705563d7e40`

```dockerfile
```

-	Layers:
	-	`sha256:9880f5698e4b9c05af6fa4706da5fb1f531e1062b8a2b83950d574fee5c603db`  
		Last Modified: Mon, 15 Jun 2026 23:27:07 GMT  
		Size: 5.3 MB (5336622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65098c60992b1f922ae914594cb595efbadba1574c64f71547c0f940d20402a`  
		Last Modified: Mon, 15 Jun 2026 23:27:06 GMT  
		Size: 23.8 KB (23755 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:b50f36baf32bab0f8cdc642ccb0eb04d29a563e07a4d9fae6d4ec5bc3f7cfb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.6 MB (372562936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d79e0c39ebf97099eeb3a68e18db5ffdc7529496ec29ef8bcad85581ea28b8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:14:54 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:14:54 GMT
ENV container oci
# Mon, 15 Jun 2026 04:14:54 GMT
COPY dir:efdade3e0178260d1a2da6ad5ac90643bb0c91f0b6715fd2f4ca2979fd79cbad in /      
# Mon, 15 Jun 2026 04:14:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:14:54 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:14:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:14:55 GMT
COPY file:e844bf29c6ce679ad36ca75749d6db974a3ec704b6b681dbf49d34fbc703890c in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:55 GMT
COPY file:e844bf29c6ce679ad36ca75749d6db974a3ec704b6b681dbf49d34fbc703890c in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:14:55 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:14:43Z" "org.opencontainers.image.created"="2026-06-15T04:14:43Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:14:43Z
# Mon, 15 Jun 2026 23:14:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:14:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:14:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:14:12 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:14:12 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Mon, 15 Jun 2026 23:16:12 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:16:19 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:16:19 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:16:19 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:16:19 GMT
CMD ["jshell"]
# Tue, 16 Jun 2026 00:05:15 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 00:05:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 00:05:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 00:05:15 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 00:05:16 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 00:06:34 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 16 Jun 2026 00:06:34 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 16 Jun 2026 00:06:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 16 Jun 2026 00:06:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 00:06:37 GMT
USER gradle
# Tue, 16 Jun 2026 00:06:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 16 Jun 2026 00:06:38 GMT
USER root
```

-	Layers:
	-	`sha256:fd098750da592cfacf74625936c645114bdb046870485748bf918ed2db1df267`  
		Last Modified: Mon, 15 Jun 2026 06:12:54 GMT  
		Size: 45.2 MB (45156026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102fbe8029dfe532f57a1538c32f741d22163601d4b4fa9e2e8a0e9afe095270`  
		Last Modified: Mon, 15 Jun 2026 23:14:51 GMT  
		Size: 30.1 MB (30096922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946a92c02b9782e278926f77f70d5a4f87f5c281310ee1e4dc65ce694e2c6813`  
		Last Modified: Mon, 15 Jun 2026 23:16:55 GMT  
		Size: 129.6 MB (129614172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0d221066edde68e144f5b71540b69440be9442e804bda591febf2b37144e44`  
		Last Modified: Mon, 15 Jun 2026 23:16:51 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c062a9b5b3f3779f0ac5cbdd8d2b8755c1426365b65ff2bebb3956591ffcca9f`  
		Last Modified: Mon, 15 Jun 2026 23:16:51 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fb7ee70dbee79ce1db8512e5378ed414b8d56ca69f3c191c731320f17fda30`  
		Last Modified: Tue, 16 Jun 2026 00:06:06 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ffdb6ec568e85a3c40dabf01a044ce5e31ee6801e28008ec0d38d135ce9072`  
		Last Modified: Tue, 16 Jun 2026 00:07:10 GMT  
		Size: 39.2 MB (39187223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28ef69e47b35a423ad58a7d3c3642504c49fc2f4679b20c7362a4853b8c3200`  
		Last Modified: Tue, 16 Jun 2026 00:07:11 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886ee513a3db54f952f0db379694f7ee113350d5a78a5a81a9518fce985e15f0`  
		Last Modified: Tue, 16 Jun 2026 00:07:07 GMT  
		Size: 35.0 KB (35007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:0c68e0d4e8d4f7348e8f672151ac7c876f80819ba40f0040d6cfb15bcf947e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ebbd807de8cac5dfa0ac5f33aec0d3d208eeab38fcd98fba2bb0f853b743c1`

```dockerfile
```

-	Layers:
	-	`sha256:2428cc41d9c4b7e23e98f30b6c753255b8f0867726845edab6198b1d137fc4c9`  
		Last Modified: Tue, 16 Jun 2026 00:07:08 GMT  
		Size: 5.3 MB (5333344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd62abfd0981d3b4f621146748ae4682a6d8f6a423193fd1c4cc7029928fae9b`  
		Last Modified: Tue, 16 Jun 2026 00:07:07 GMT  
		Size: 23.6 KB (23645 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:420f4a7111df416fcd118c512e262d759602f168feab454268867e2e422039c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.6 MB (355592163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0c11ac0b4603bb0771831db51455dedd06478f3468b3e3b392c0d00e839b5d`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL maintainer="Red Hat, Inc."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL vendor="Red Hat, Inc."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.8"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL io.openshift.expose-services=""
# Mon, 15 Jun 2026 04:18:01 GMT
LABEL io.openshift.tags="minimal rhel9"
# Mon, 15 Jun 2026 04:18:01 GMT
ENV container oci
# Mon, 15 Jun 2026 04:18:01 GMT
COPY dir:b287442ff3a1305f30c768257fb405a05247fad637bf642752f1eb5c150e583c in /      
# Mon, 15 Jun 2026 04:18:01 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Mon, 15 Jun 2026 04:18:01 GMT
CMD ["/bin/bash"]
# Mon, 15 Jun 2026 04:18:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Mon, 15 Jun 2026 04:18:01 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Mon, 15 Jun 2026 04:18:02 GMT
COPY file:8c615175ae26448d1bab1087e5b4f0afb27d6d1d3930dbd033fa26b49547a2f9 in /usr/share/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:18:02 GMT
COPY file:8c615175ae26448d1bab1087e5b4f0afb27d6d1d3930dbd033fa26b49547a2f9 in /root/buildinfo/labels.json      
# Mon, 15 Jun 2026 04:18:02 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="92938083b76077787596c980f5cdc39e89c50a24" "org.opencontainers.image.revision"="92938083b76077787596c980f5cdc39e89c50a24" "build-date"="2026-06-15T04:17:50Z" "org.opencontainers.image.created"="2026-06-15T04:17:50Z" "release"="1781496742"org.opencontainers.image.revision=92938083b76077787596c980f5cdc39e89c50a24,org.opencontainers.image.created=2026-06-15T04:17:50Z
# Mon, 15 Jun 2026 23:12:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 15 Jun 2026 23:12:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jun 2026 23:12:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 15 Jun 2026 23:12:42 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Mon, 15 Jun 2026 23:12:42 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Mon, 15 Jun 2026 23:34:26 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='257f4d39e060658fc2eb89a803ca43b3f337e64e253f2d94ebae1d85c9ef5f69';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.31_11.tar.gz';          ;;        ppc64le)          ESUM='e473d10c3c44f67301fd90abd9e4b7ae312eae8a2399b333fcf4179daf35a743';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.31_11.tar.gz';          ;;        s390x)          ESUM='4d3709cdc03de1a00f14f530c2ebad1883d9bcc8a556fc419f083bec87b4687a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.31_11.tar.gz';          ;;        x86_64)          ESUM='1e9de64586b519c0a981319489257cabedd9457599f3823424a87c3158fbe939';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.31%2B11/OpenJDK11U-jdk_x64_linux_hotspot_11.0.31_11.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Mon, 15 Jun 2026 23:34:28 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 15 Jun 2026 23:34:28 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 15 Jun 2026 23:34:28 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 15 Jun 2026 23:34:28 GMT
CMD ["jshell"]
# Tue, 16 Jun 2026 00:00:23 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 00:00:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 00:00:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 00:00:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 00:00:23 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 00:00:58 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 16 Jun 2026 00:00:58 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 16 Jun 2026 00:00:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 16 Jun 2026 00:01:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 00:01:01 GMT
USER gradle
# Tue, 16 Jun 2026 00:01:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 16 Jun 2026 00:01:02 GMT
USER root
```

-	Layers:
	-	`sha256:99902732bbc0758252faa428c8bd627fb473cdca6d03f791fd4b177c4a5de314`  
		Last Modified: Mon, 15 Jun 2026 06:12:36 GMT  
		Size: 38.8 MB (38806856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d124567964b233fa0f2f2c3220acab3cf5090a6eea57d13aaa5d82fbbe0c8ce3`  
		Last Modified: Mon, 15 Jun 2026 23:13:09 GMT  
		Size: 27.7 MB (27692083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e91075ced9478683d44e5868560b2adebb666c8fcc10317dabb49bb331a139`  
		Last Modified: Mon, 15 Jun 2026 23:34:56 GMT  
		Size: 123.1 MB (123061431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d671e909f0c954ab302774ce0e286e190a4bed8e55ebf1b38d81bae7f0b74323`  
		Last Modified: Mon, 15 Jun 2026 23:34:54 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5047fd52d7b2a22222d352510e46de6e25bdd99e640227168387bfcee8fd5b20`  
		Last Modified: Mon, 15 Jun 2026 23:34:54 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c969e7d26aa3ccdd0e2c2152bda5bac4f4b6cd78f73546d76e2862013fbdbe94`  
		Last Modified: Tue, 16 Jun 2026 00:01:03 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496e3faa127fa1c562032ea4f0cad6c8adfdda1d94e070c17b9f2037f7ffcf96`  
		Last Modified: Tue, 16 Jun 2026 00:01:27 GMT  
		Size: 37.5 MB (37523201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403141c5cc0505da03d1eb02d5acdb88687e3a2f1ab630abb3c5a2f91cecca15`  
		Last Modified: Tue, 16 Jun 2026 00:01:28 GMT  
		Size: 128.5 MB (128469420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494404035e99a7a06350e7e76a211a63d1e7ef2bf3412bae8761eb2500c4ce46`  
		Last Modified: Tue, 16 Jun 2026 00:01:26 GMT  
		Size: 35.0 KB (35009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:115f15f52304b57e7f735125a493c94f88617a2eedd76088de63cb73a3d080a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5346794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337700b5d2e4b3a8435e2d39c6c1c4922761d6c61ee454b10d3b8fad1aaae84b`

```dockerfile
```

-	Layers:
	-	`sha256:72202e5ddc5152a8fece9ed2e20f8e71e17dd5e1e584a0dccee3fe5b541faaa5`  
		Last Modified: Tue, 16 Jun 2026 00:01:26 GMT  
		Size: 5.3 MB (5323211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:194a3b17af809d7ec4b7312deedc3d3e00ca023059ce313e76bd66567e59452f`  
		Last Modified: Tue, 16 Jun 2026 00:01:25 GMT  
		Size: 23.6 KB (23583 bytes)  
		MIME: application/vnd.in-toto+json
