## `gradle:6-jdk11-ubi`

```console
$ docker pull gradle@sha256:19c0536e3f4d2dcb23d2e76d2948227fe833fda13adb32c4757ccf201256e1db
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

### `gradle:6-jdk11-ubi` - linux; amd64

```console
$ docker pull gradle@sha256:64663001da79768de334a30694965e631d9966f3c33c2d353980a3d4904950a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.5 MB (357475949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7cc14354942a3a9538086f3e632668e4b2f3db668ac2db49a467d71372a5b6`
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
# Tue, 14 Apr 2026 20:45:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:45:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:45:32 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:45:32 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:45:32 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 20:45:38 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:39 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:39 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:39 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:59:12 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:59:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:59:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:59:12 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:59:12 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:59:16 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:59:16 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 14 Apr 2026 20:59:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 14 Apr 2026 21:00:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 21:00:56 GMT
USER gradle
# Tue, 14 Apr 2026 21:00:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 21:00:57 GMT
USER root
```

-	Layers:
	-	`sha256:b1ed13c5ef0ac6dbcd255a5c1be9e3c9c2903872aa4ae5fa877850a48fdaee26`  
		Last Modified: Mon, 13 Apr 2026 19:17:03 GMT  
		Size: 40.0 MB (40016560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fb22d429ca0142fa2aaf4dd83e368753d8474e70b668e50b10f310fa526751`  
		Last Modified: Tue, 14 Apr 2026 20:45:57 GMT  
		Size: 30.4 MB (30369635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dee96365b2b8af6fa5c79f607e4d129e48dc6280097dda21ce3e778ca645614`  
		Last Modified: Tue, 14 Apr 2026 20:45:59 GMT  
		Size: 142.3 MB (142263242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ccab4fdd8c4bc2a852f1fa7e62d6b9c2a9e78f9165b072e6daf7bec93e1032`  
		Last Modified: Tue, 14 Apr 2026 20:45:55 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8dfe926bc9d0a59836cc3c4426e3069f970c168eeb7974e6283e040656daa3`  
		Last Modified: Tue, 14 Apr 2026 20:45:46 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc040b1b3397a248faa0d4603657a02f5e9408f93993a3c8607f1f17c8275d0`  
		Last Modified: Tue, 14 Apr 2026 20:59:34 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437d400be8dd3d780f279d0a15619ba1f22d74fbed07dbdd191e98da737db723`  
		Last Modified: Tue, 14 Apr 2026 20:59:35 GMT  
		Size: 36.7 MB (36694413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f280cb125131215df5633e7f928c65ed99c7e302bbd415478d5c92e6f7ad7387`  
		Last Modified: Tue, 14 Apr 2026 21:01:12 GMT  
		Size: 107.7 MB (107696669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9615ad9c8458e58cace26e3383411dde2b12653ab71f3f00f00b5f2a81fe0a87`  
		Last Modified: Tue, 14 Apr 2026 21:01:10 GMT  
		Size: 431.3 KB (431277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:f83bf30c18b58ee56ba12a2cf85de27832c62f8dc4eb69e432b8ea092cf80a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5475e007f74f6398623a62499b2789c05196a994b60f01c71adda4be226e732`

```dockerfile
```

-	Layers:
	-	`sha256:514c226fabf7cfb29acbf5a16d171477e8f721afe514f90f0c90dd8937709614`  
		Last Modified: Tue, 14 Apr 2026 21:01:10 GMT  
		Size: 5.3 MB (5316182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54407a8dfbb7bc8619928b85b30323cdfae66008fb60732b6dac781bca1d54c2`  
		Last Modified: Tue, 14 Apr 2026 21:01:10 GMT  
		Size: 23.6 KB (23579 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:717f546286dff8a9db6f13ae468836305d966407a882a8f4f524ad154f984cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352109271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a47c7ccde3513e53bd00860855fad93fcdf5c9624b09628e5194964dbb4104b`
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
# Tue, 14 Apr 2026 20:45:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 Apr 2026 20:45:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 20:45:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 14 Apr 2026 20:45:23 GMT
RUN set -eux;     microdnf install -y         gzip         tar         binutils         tzdata         wget         ca-certificates         openssl         fontconfig         glibc-langpack-en     ;     microdnf clean all # buildkit
# Tue, 14 Apr 2026 20:45:23 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 20:45:34 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:35 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:35 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:35 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:56:24 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:56:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:56:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:56:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:56:24 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:56:28 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:56:28 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 14 Apr 2026 20:56:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 14 Apr 2026 20:56:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:56:31 GMT
USER gradle
# Tue, 14 Apr 2026 20:56:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:56:31 GMT
USER root
```

-	Layers:
	-	`sha256:f7c1b31b8294524de5dff6550312e7fc2a074a842daad5dd610d9bfdab56527d`  
		Last Modified: Mon, 13 Apr 2026 19:17:00 GMT  
		Size: 38.2 MB (38200105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681efa422a1547a4042f595ef92f8572b64e95767fdd974ef4402e56f6bb68b9`  
		Last Modified: Tue, 14 Apr 2026 20:45:53 GMT  
		Size: 30.8 MB (30797611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c33c8f48a72f485a25866f11a226366e1754e5c811979f72fec008e953d92c6`  
		Last Modified: Tue, 14 Apr 2026 20:45:56 GMT  
		Size: 139.0 MB (138959720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef53e10a48dbd6a09dda5d09ea763908d76acc48bb61e9e1348d8f52bcf3f0`  
		Last Modified: Tue, 14 Apr 2026 20:45:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909ad6772ab10804930be2a0e0eb5833462da9a14f7acdcf44637420071653fc`  
		Last Modified: Tue, 14 Apr 2026 20:45:36 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a728a49707094327cef8d0a9bd50f4d7769370bdd2410d4eb68a78f397ae47d`  
		Last Modified: Tue, 14 Apr 2026 20:56:46 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d357e08258fd8cc909a37e032ac37525be7416858092da56b946f3ae1b7a127`  
		Last Modified: Tue, 14 Apr 2026 20:56:48 GMT  
		Size: 36.0 MB (36025986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2d011b0a2df16297fe7cfb80d5fb963278338769278a4fe86db377682502a6`  
		Last Modified: Tue, 14 Apr 2026 20:56:50 GMT  
		Size: 107.7 MB (107696673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c97b67df55b36a16bc5f02a8550d42c8f6f66d0338abbd062be9e95ee78fa8`  
		Last Modified: Tue, 14 Apr 2026 20:56:46 GMT  
		Size: 425.0 KB (425018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:fb83dd99804fabcd3f017159a6acc77d80bfafc534946efc9ce5d3853d332d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c178a89600fa78734fdaf8f6e7993deb3887a5b4cd303ee2591885ba3f8540b0`

```dockerfile
```

-	Layers:
	-	`sha256:fd27e75ead8a16d24677c846766ebad2141cc7182c02a99bffeeda8165cbefa1`  
		Last Modified: Tue, 14 Apr 2026 20:56:47 GMT  
		Size: 5.3 MB (5316206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7348ba6579fea4b9b7f083d103b300f81916e84f4c1404d4925af7d19c278e9a`  
		Last Modified: Tue, 14 Apr 2026 20:56:46 GMT  
		Size: 23.8 KB (23753 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi` - linux; ppc64le

```console
$ docker pull gradle@sha256:fe080d78da8b937bcc8378404c7fd46ce04d7f10dfd040976b441c873517c266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.5 MB (352459125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3228bb98dec7f65f2ad2eaa0ba1f17e6d912cf804560b071322211862ceb0538`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 20:45:08 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:45:11 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:45:12 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:45:12 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:45:12 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:57:47 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:57:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:57:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:57:47 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:57:50 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:58:05 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:58:05 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 14 Apr 2026 20:58:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 14 Apr 2026 21:02:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 21:02:10 GMT
USER gradle
# Tue, 14 Apr 2026 21:02:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 21:02:12 GMT
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
	-	`sha256:c5e6b6fd91f7e9fc55ff60b6f38c767be21fdcb566b6b7b1638958319d97e14c`  
		Last Modified: Tue, 14 Apr 2026 20:45:44 GMT  
		Size: 129.5 MB (129499207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12db4c175ab3e86f31f3abd8f859970116e3aa96a1c9ffafd1e59dc0820f2b2`  
		Last Modified: Tue, 14 Apr 2026 20:45:38 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02baed26fbd11a809fbe16668017f567ef63d2436ab10d3efaf14bbdb67d6cb3`  
		Last Modified: Tue, 14 Apr 2026 20:45:38 GMT  
		Size: 2.3 KB (2289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71087b66eaa2f76f12caf597d5fed16b75f4ab857ee4c7597974fb31fcad209`  
		Last Modified: Tue, 14 Apr 2026 20:58:53 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1380863ad69753ee4d7dc8af873bd368583d85d0a087b63f3f23325aaa7bd35e`  
		Last Modified: Tue, 14 Apr 2026 20:58:56 GMT  
		Size: 37.9 MB (37930855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98bd102f2653f69a28868d0b3142f88f1b41193210b9656c4dd9ae969eb2757e`  
		Last Modified: Tue, 14 Apr 2026 21:02:47 GMT  
		Size: 107.7 MB (107696652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abd087fc22086c989052c3c38d7168a18a7e2e5a5e9d67c9d28b0e1959e5211`  
		Last Modified: Tue, 14 Apr 2026 21:02:42 GMT  
		Size: 35.0 KB (34982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:bfa1c3db660e613df78bd34d175f1d1b24c5b49c3cefcbba51976872080195a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610321fc1a302437b5ec24548fff97e1382494adbbb4765faaac95f011fbf16a`

```dockerfile
```

-	Layers:
	-	`sha256:1be3dc8823dff80772649edb5219acc96672a638fb7d6587bd158c74acb93dba`  
		Last Modified: Tue, 14 Apr 2026 21:02:43 GMT  
		Size: 5.3 MB (5312890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:641c157dadf84a365bb5e760ef03930bbbf0be55a23f60b4c146a904d6cb10f9`  
		Last Modified: Tue, 14 Apr 2026 21:02:43 GMT  
		Size: 23.6 KB (23641 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-ubi` - linux; s390x

```console
$ docker pull gradle@sha256:24b535b1e52da241cee4b78eb03f099a1f3445b9873b9f0b81a120f083408324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.5 MB (335543672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395da91898124e47ac681424c319da062c7d319b0a249fd0b757c0e0229c0848`
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
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 20:44:21 GMT
RUN set -eux;     ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)";     case "${ARCH}" in        aarch64)          ESUM='3c8fb6754deced4e08a03524b6af1df4f3df451f1832f3dcd3a6848fd54b8d08';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.30_7.tar.gz';          ;;        ppc64le)          ESUM='6ef8f74f92b1d8723392cb6b90351e5f8fb0f94c29c351b5b407bdf46f9af76c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.30_7.tar.gz';          ;;        s390x)          ESUM='79869c9f79e22266efcb3e086bcb9bbd8d58605693f742e5785f215c0fa249ab';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.30_7.tar.gz';          ;;        x86_64)          ESUM='1911fa4010d59985d4cba9f4295c704ae64d08dfc3c2d5747bbc18655b1e911a';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.30%2B7/OpenJDK11U-jdk_x64_linux_hotspot_11.0.30_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 14 Apr 2026 20:44:23 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 14 Apr 2026 20:44:23 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 14 Apr 2026 20:44:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 14 Apr 2026 20:44:23 GMT
CMD ["jshell"]
# Tue, 14 Apr 2026 20:56:20 GMT
CMD ["gradle"]
# Tue, 14 Apr 2026 20:56:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 14 Apr 2026 20:56:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 101 gradle     && useradd --system --gid gradle --uid 101 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 14 Apr 2026 20:56:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 14 Apr 2026 20:56:20 GMT
WORKDIR /home/gradle
# Tue, 14 Apr 2026 20:56:24 GMT
RUN set -o errexit -o nounset     && microdnf install -y         make                 findutils                 unzip         which                 git         git-lfs         subversion     && microdnf clean all         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which svn # buildkit
# Tue, 14 Apr 2026 20:56:24 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 14 Apr 2026 20:56:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 14 Apr 2026 20:56:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 14 Apr 2026 20:56:28 GMT
USER gradle
# Tue, 14 Apr 2026 20:56:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 14 Apr 2026 20:56:28 GMT
USER root
```

-	Layers:
	-	`sha256:188bc35e04514e4f35552e12dec8be6787ac365d49a3ea7fa542d4acf61bfd45`  
		Last Modified: Tue, 14 Apr 2026 00:13:48 GMT  
		Size: 38.1 MB (38114710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae9687a0b2d77e6f626096a581f6657be9436e53837fecdd37bd78516ce7aa`  
		Last Modified: Tue, 14 Apr 2026 20:44:47 GMT  
		Size: 30.4 MB (30388978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e6141d996581c02d418d7fced5d885f95e9857813ce0aa81283cef5fe4f54f`  
		Last Modified: Tue, 14 Apr 2026 20:44:49 GMT  
		Size: 123.0 MB (122972667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f659d1bca244f7dcbe2311334cd7d74b483b44257e3b5377d01c721b4800664`  
		Last Modified: Tue, 14 Apr 2026 20:44:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423e9468fdedbdf89c99f9e0e1cee9f199858b79d56365aea5ced004a41ed6ef`  
		Last Modified: Tue, 14 Apr 2026 20:44:46 GMT  
		Size: 2.3 KB (2290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0194f40839bbc863180ff2379e6f47eca92f2072c2a1eed935be2cab484d37`  
		Last Modified: Tue, 14 Apr 2026 20:56:52 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fa6dd013a835796d0704201e13568da4058bc38421508584b4a4ecfd4b593d`  
		Last Modified: Tue, 14 Apr 2026 20:56:53 GMT  
		Size: 36.3 MB (36331502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5400602cf71e5d3d12b670b2e982879d6bcd87f0cbcce969c154b3e05b19852`  
		Last Modified: Tue, 14 Apr 2026 20:56:55 GMT  
		Size: 107.7 MB (107696672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90009b9b1f292603a7ae80e77e86deffcaadf04c8904572ca50be96d3e76848`  
		Last Modified: Tue, 14 Apr 2026 20:56:52 GMT  
		Size: 35.0 KB (34979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-ubi` - unknown; unknown

```console
$ docker pull gradle@sha256:3ddb771b679b2029adbb6dd28f246206e348f0240aab589579f6938cff59f913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5326370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fea5b67a04d7bf878827ac30c2953dd3382e14978d3e795000092a7d1389be`

```dockerfile
```

-	Layers:
	-	`sha256:ab3aaf511fb4af823973d8a94fc373a76244114f4ccbdbcb87a69f4e3205fc89`  
		Last Modified: Tue, 14 Apr 2026 20:56:52 GMT  
		Size: 5.3 MB (5302791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2edc822836828bd79e179e1310d2d6b4fb44cadf32f83c104d11bcac2bb54d0b`  
		Last Modified: Tue, 14 Apr 2026 20:56:52 GMT  
		Size: 23.6 KB (23579 bytes)  
		MIME: application/vnd.in-toto+json
