## `gradle:8-jdk11-ubi9`

```console
$ docker pull gradle@sha256:8f1ca3359acfc32e02d35dda999f7574c4615ee3bae783d7679d3cc5d5e3e5a9
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
$ docker pull gradle@sha256:4f2b0d3e5f4037a149ec3049f309ae25ec794b9727f83a9c38bd898bee9ccfa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 MB (386852258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02169114cc295e31a319f7edf7dc27c649f379d203acc987d5ad6fb44621ce30`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 00:16:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:16:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:16:51 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:16:51 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:16:51 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Fri, 20 Mar 2026 00:16:59 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:17:00 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:17:00 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:17:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:17:00 GMT
CMD ["jshell"]
# Fri, 20 Mar 2026 01:11:12 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 01:11:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 01:11:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 01:11:12 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 01:11:12 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 01:11:17 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 01:11:17 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 20 Mar 2026 01:11:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 20 Mar 2026 01:11:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 01:11:20 GMT
USER gradle
# Fri, 20 Mar 2026 01:11:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Mar 2026 01:11:21 GMT
USER root
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b966be76c27145f6d0e6579c4a40d4c35a50ee0a1979b2eec933cb408b0aa`  
		Last Modified: Fri, 20 Mar 2026 00:17:18 GMT  
		Size: 30.4 MB (30393068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4ff4e42928f223fcb5932f494735a0d87bbf21ca18d45774b1032a7e219d20`  
		Last Modified: Fri, 20 Mar 2026 00:17:20 GMT  
		Size: 142.3 MB (142263283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57d6cd37e733fc698f83f0ab0c3d820b41322c6e8766c8135c96ed65f6ae4c7`  
		Last Modified: Fri, 20 Mar 2026 00:17:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b19e56fea1f792f5e9e3f9500f25b2b2778c63fd68d3f98d932d76aa70bc0b`  
		Last Modified: Fri, 20 Mar 2026 00:17:17 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdc16f4b5ed74e3ee624adc7ced7748127a92299573b9e09be59d4e37cfaafc`  
		Last Modified: Fri, 20 Mar 2026 01:11:37 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db741887c71148d222250db43d0e7a1703fa53282d3bc3dd008631fff1164afb`  
		Last Modified: Fri, 20 Mar 2026 01:11:39 GMT  
		Size: 36.7 MB (36717449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de2709db28b5e0479e346dfd43c50f8210138278f702e1d1fd8f9bf45dbd688`  
		Last Modified: Fri, 20 Mar 2026 01:11:41 GMT  
		Size: 137.4 MB (137388273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40fa48ae219c5f7e91e8f49a62b55796daee5b1618819dd831bc8ffd627f5126`  
		Last Modified: Fri, 20 Mar 2026 01:11:38 GMT  
		Size: 54.9 KB (54908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:0bb17f0d04f951bbcbfc1571a8dbab46b44eda29a36a83cb85db9ab139d2e030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143e4aa114742589051f607e7835c6556b55fbc39cbe8324b9f79b0523074b87`

```dockerfile
```

-	Layers:
	-	`sha256:8891a1829b83805e492fb4ef83bb586a1ef3af391bc55a733814b08215ed9366`  
		Last Modified: Fri, 20 Mar 2026 01:11:38 GMT  
		Size: 5.4 MB (5424037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:118a85b1e93d61262fdbe178dceec0cc96eaca22c15d41e456c4058eb19c601a`  
		Last Modified: Fri, 20 Mar 2026 01:11:37 GMT  
		Size: 24.2 KB (24162 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi9` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:566f16403aad740c3c626b8bd6ced3a6c9b879c04f29709a693db025c0571caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 MB (381494939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be579ca4f1f0028945f152cfcd84646c56678cdf0e0251fd6f43e370bc2e9005`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 00:13:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:13:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:13:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:13:37 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:13:37 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Fri, 20 Mar 2026 00:14:11 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:14:12 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:14:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:14:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:14:12 GMT
CMD ["jshell"]
# Fri, 20 Mar 2026 01:11:59 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 01:11:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 01:11:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 01:11:59 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 01:11:59 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 01:12:03 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 01:12:03 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 20 Mar 2026 01:12:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 20 Mar 2026 01:12:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 01:12:06 GMT
USER gradle
# Fri, 20 Mar 2026 01:12:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Mar 2026 01:12:07 GMT
USER root
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e770bd615d1aae6c3e96a1968ff17609f1fcbfdb62794b41785ce77cf9c6b9a1`  
		Last Modified: Fri, 20 Mar 2026 00:13:56 GMT  
		Size: 30.8 MB (30824619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad39c239a211d23cc2b37489dc80406eb4ee788d26841ddf3b1c0ddb561779f`  
		Last Modified: Fri, 20 Mar 2026 00:14:30 GMT  
		Size: 139.0 MB (138959727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55053b551a3190ab274fc71c1a0cbd4c113c2250c2680c3e7e302b93980e071`  
		Last Modified: Fri, 20 Mar 2026 00:14:26 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551a54df41ac49d1e8afaa0df954c53b150e04568aaa305cb4f7bcaa2143137`  
		Last Modified: Fri, 20 Mar 2026 00:14:27 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6c4cde2b68f22490b76bfb3324e1038278f5c086409dacb905f78d644f3af4`  
		Last Modified: Fri, 20 Mar 2026 01:12:24 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d108f1373d5faee4ab4de4c8927f61321c4579dd1ba3d914575e333de1064467`  
		Last Modified: Fri, 20 Mar 2026 01:12:25 GMT  
		Size: 36.1 MB (36053735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2dd04f8af09f13a1a2919fc5964de780053d1d44c76fa23847f735a14e1a8b`  
		Last Modified: Fri, 20 Mar 2026 01:12:27 GMT  
		Size: 137.4 MB (137388273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ff6f9410853ae1c6d739025ddde9a3d2c1b207173c1bb3b4dcc6e72cc5a433`  
		Last Modified: Fri, 20 Mar 2026 01:12:23 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:654c5b87488fb114461dc37bea810546f1e4bd529c6287ffffdbef0575f4df87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569b0b2dc567c7329f0b8bef525870520d81d1db534f87381e7e48f7f2058b6d`

```dockerfile
```

-	Layers:
	-	`sha256:cb5289fc9c278ddbc1bf8226ac0a1f8d11efcaeb644e297bca361ab58f930e8a`  
		Last Modified: Fri, 20 Mar 2026 01:12:24 GMT  
		Size: 5.4 MB (5424085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b01ef6f994534f7e006ce84edb21082ef84c9c4ecde521aa6054cb7e4558e1`  
		Last Modified: Fri, 20 Mar 2026 01:12:24 GMT  
		Size: 24.4 KB (24360 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi9` - linux; ppc64le

```console
$ docker pull gradle@sha256:18296d978de6bfd9c0ca4195013bac23d0b199b18365962b0fe80885f43e89cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 MB (382216889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af5ef0bee5a3ee1dc2b7a035aa7b36bd20fc108a57f3fc84d5bb60cb6214db6`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:06 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:06 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:07 GMT
COPY dir:212bcd6ca40edbbce9f77f229da8875e11d96069d070bf3fb59e68c3ea39f651 in /      
# Thu, 19 Mar 2026 17:04:07 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:07 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:07 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:07 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:07 GMT
COPY file:534e39f6085eb0cb384d19a91779b0b89650bb4a0b7dfa938788378ee234529d in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:07 GMT
COPY file:534e39f6085eb0cb384d19a91779b0b89650bb4a0b7dfa938788378ee234529d in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:08 GMT
LABEL "architecture"="ppc64le" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:03:56Z" "org.opencontainers.image.created"="2026-03-19T17:03:56Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:03:56Z
# Fri, 20 Mar 2026 00:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:01:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:01:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:01:59 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:01:59 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Fri, 20 Mar 2026 00:04:06 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:04:09 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:04:10 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:04:10 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:04:10 GMT
CMD ["jshell"]
# Fri, 20 Mar 2026 00:25:23 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 00:25:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 00:25:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 00:25:23 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 00:25:24 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 00:26:02 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 00:26:02 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 20 Mar 2026 00:26:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 20 Mar 2026 00:26:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 00:26:08 GMT
USER gradle
# Fri, 20 Mar 2026 00:26:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Mar 2026 00:26:10 GMT
USER root
```

-	Layers:
	-	`sha256:e27f930d68b2ba9e0fc573a4b041546b9a188e745bc064293a4e374cef018bf9`  
		Last Modified: Thu, 19 Mar 2026 18:10:52 GMT  
		Size: 44.5 MB (44462958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1402d8c5d4540db2cd7be54111e389a08d3d4bdf8a6cea11e1797da30faa69b`  
		Last Modified: Fri, 20 Mar 2026 00:02:44 GMT  
		Size: 32.9 MB (32875980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b584986a1089161146536fd97b25684076f182c913e488f35fb83025e2d7b446`  
		Last Modified: Fri, 20 Mar 2026 00:04:43 GMT  
		Size: 129.5 MB (129499185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3123d922162b75b6981e85f62b8e793306e72150136d32a17c29dc513efc59ab`  
		Last Modified: Fri, 20 Mar 2026 00:04:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174b07663936d1ced0ddabee88a2677b172a690bd8d049259f91bac693e3487a`  
		Last Modified: Fri, 20 Mar 2026 00:04:40 GMT  
		Size: 2.3 KB (2292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bf31f1cdb524712631d8a3041e079dc641f0e75e783ff6c8c5514bb7fabb4a`  
		Last Modified: Fri, 20 Mar 2026 00:27:09 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2089722662101fae5529c72bac55f5578d562cf40e107049ba0157d3888a5aaf`  
		Last Modified: Fri, 20 Mar 2026 00:27:12 GMT  
		Size: 38.0 MB (37951316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d6621fa699fe8c2669c71ee50f87878a5553a3ade7696882ae3cac39895937`  
		Last Modified: Fri, 20 Mar 2026 00:27:14 GMT  
		Size: 137.4 MB (137388276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5336ea6c55edbc33c1f2efe45e7a295ccc3c9aee7dbede34df1f7c9bfd362061`  
		Last Modified: Fri, 20 Mar 2026 00:27:09 GMT  
		Size: 35.0 KB (35013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:496be9e2cdbec81161cec17c7bb17ad6367ad9110dac3225141ea1be244b01e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f7a3683173b4a8226a6c46b62ce3d3056e53534f55b5f47d96feded306574b`

```dockerfile
```

-	Layers:
	-	`sha256:9174854583b82381c2f546a62f23f6c371eb10213652c6272a3a84e497271348`  
		Last Modified: Fri, 20 Mar 2026 00:27:10 GMT  
		Size: 5.4 MB (5420757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f0210cc0fd3c13fdbdb8f2de90267f61abf8c8e1a239b2f6f51ceb177b3b6e1`  
		Last Modified: Fri, 20 Mar 2026 00:27:09 GMT  
		Size: 24.3 KB (24273 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-ubi9` - linux; s390x

```console
$ docker pull gradle@sha256:1fe950b57b298657d931bdf081819b6032ae468e9a3db60a81c05001fb3f1dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365278760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6188d4bc25d8926812f8584fb546db7266b5aaddfc2f82aa6e27522804b5eb2b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:22:13 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:22:13 GMT
ENV container oci
# Thu, 19 Mar 2026 17:22:14 GMT
COPY dir:47bb3b5a1fb1490a7f21d445cf75c47d24677e64c255eb447ee5eb808233d94f in /      
# Thu, 19 Mar 2026 17:22:14 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:22:14 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:22:14 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:22:14 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:22:14 GMT
COPY file:fd81d1e2b133f657ce0ad41efef4e9473e1fd2c70d3a505d8e6d106665117e8f in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:22:14 GMT
COPY file:fd81d1e2b133f657ce0ad41efef4e9473e1fd2c70d3a505d8e6d106665117e8f in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:22:14 GMT
LABEL "architecture"="s390x" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:22:01Z" "org.opencontainers.image.created"="2026-03-19T17:22:01Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:22:01Z
# Fri, 20 Mar 2026 00:01:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 20 Mar 2026 00:01:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:01:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 20 Mar 2026 00:01:44 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:01:44 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Fri, 20 Mar 2026 00:01:51 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Fri, 20 Mar 2026 00:01:53 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Fri, 20 Mar 2026 00:01:53 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Fri, 20 Mar 2026 00:01:53 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 20 Mar 2026 00:01:53 GMT
CMD ["jshell"]
# Fri, 20 Mar 2026 00:12:20 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 00:12:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 00:12:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 00:12:20 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 00:12:20 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 00:12:25 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Fri, 20 Mar 2026 00:12:25 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 20 Mar 2026 00:12:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 20 Mar 2026 00:12:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 00:12:29 GMT
USER gradle
# Fri, 20 Mar 2026 00:12:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Mar 2026 00:12:29 GMT
USER root
```

-	Layers:
	-	`sha256:eedf11da6ea06bb6f639e39517d50c96ce1d675b360c116c68fdbccc4a25b815`  
		Last Modified: Thu, 19 Mar 2026 18:10:37 GMT  
		Size: 38.1 MB (38115175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25ac3158e49698ffa6a8276d4c61a8590d2746c7374dd389fd8873428301658`  
		Last Modified: Fri, 20 Mar 2026 00:02:16 GMT  
		Size: 30.4 MB (30411913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c90433412ad468a40c2b7a4645480c475066fa12a62ef0b05bffec95ddbfd6`  
		Last Modified: Fri, 20 Mar 2026 00:02:18 GMT  
		Size: 123.0 MB (122972699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849e1b82145cda671333eaeffae88c2bc98c86805463196153626be7eb2a69de`  
		Last Modified: Fri, 20 Mar 2026 00:02:15 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29bc30a0e31045c8c347e2dabe9ea6175c0b9627afbf420e5d52bb1f2665d70`  
		Last Modified: Fri, 20 Mar 2026 00:02:16 GMT  
		Size: 2.3 KB (2291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cafeafed30c854a60d33d638d05d988ec62c62369b08f5900eb6e9b833af18d`  
		Last Modified: Fri, 20 Mar 2026 00:12:54 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe04947226207421dfc1b05a197f58a3a699c5d338cc7ce250a2ec57e86d91a`  
		Last Modified: Fri, 20 Mar 2026 00:12:55 GMT  
		Size: 36.4 MB (36351513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed7bb88abb836545a26986129a046e39c0fe36c9e52c7938b617ebe246682ad`  
		Last Modified: Fri, 20 Mar 2026 00:12:58 GMT  
		Size: 137.4 MB (137388299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff946b7327c4b36acaaaf5b1876d983331b7e14016f7c36b82eafa9c052c8d`  
		Last Modified: Fri, 20 Mar 2026 00:12:55 GMT  
		Size: 35.0 KB (35003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-ubi9` - unknown; unknown

```console
$ docker pull gradle@sha256:3fc6e028feb9cf32afaab17fe35c12ee4febe243e6ae678013b0b211121b37ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5434845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136ac77f99f45583bb7dd445d64bf9f2bb6d9070b1a6df44f6661ae7015e0c6d`

```dockerfile
```

-	Layers:
	-	`sha256:fe23599cfbfb91aab638baeef79937c8ce26f5cfa8b35fdadea9a6ca2af9cb4f`  
		Last Modified: Fri, 20 Mar 2026 00:12:55 GMT  
		Size: 5.4 MB (5410646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58501f5c413e36c8c661e79f749bfc64cc965bac131b8cf86456912c384df21c`  
		Last Modified: Fri, 20 Mar 2026 00:12:54 GMT  
		Size: 24.2 KB (24199 bytes)  
		MIME: application/vnd.in-toto+json
