## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:e9a221dbd4c14497f1faafc35876a9b13140a8ed6713836bf7b21146d8cb27ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:c78dda50505197b7288cc818fb00dd7be2e1fc2e23de196cc7aa871d98ddaaba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434458826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a98f200ba281ff5fe4300f31c50175a2ac958771fbc2a250c84da8f4bb91b4d`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:07:56 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:07:56 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:07:56 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:07:56 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:07:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 17:29:22 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:29:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:29:22 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:29:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:29:23 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:29:23 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:29:23 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 17:29:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 17:29:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:29:25 GMT
USER gradle
# Fri, 03 Apr 2026 17:29:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 17:29:26 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d132f643ccc51adef2f8116c0839f1a3410d13832ab23aab291b4c6648c895`  
		Last Modified: Fri, 03 Apr 2026 17:08:16 GMT  
		Size: 156.9 MB (156911186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faba53cba3d4647312aa93a3f94b55856903b7c125fb39befd454997c794a249`  
		Last Modified: Fri, 03 Apr 2026 17:29:55 GMT  
		Size: 86.1 MB (86069706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556f5360746d2d333a14aa53f162e464af586522ecffe414ecf5de3294ff5566`  
		Last Modified: Fri, 03 Apr 2026 17:29:52 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112eef2f107b215a65027fd9e6b0b4d4e90becbf388d99f557f9325d470a7503`  
		Last Modified: Fri, 03 Apr 2026 17:29:56 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f904776c206bb4d88761d16aa5bbe640494dc086acd78479bd3399a6e4a5ff`  
		Last Modified: Fri, 03 Apr 2026 17:29:52 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:d06356504e3e3f92d2fa97574346bf19a29eb70b839ec31b7409f82f4b018da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11360656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b280c7eb208b5225104f385cbaa0004f4ceb2c08867a7fefb8217a2b54a8334a`

```dockerfile
```

-	Layers:
	-	`sha256:7407b9189cd2627b6033d2a3054eb3ca2da0d2ce1c79d4252e89528dde4fc2d2`  
		Last Modified: Fri, 03 Apr 2026 17:29:52 GMT  
		Size: 11.3 MB (11339929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881ddfb5604ded4ad599bcce25feb4a8908079352b628a288608a2a680da35a9`  
		Last Modified: Fri, 03 Apr 2026 17:29:52 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a4e4db4e8a6da60425dbba7fc0ec837bb6c92f899ade019442851aa66bcf2c3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.7 MB (431664211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e2ffb749f8dff9248df0e8a93dc8f4700a1cf404c74f674905d0dc856ad56e`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:15:23 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 17:15:23 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:15:23 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:15:23 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:15:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 17:29:32 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:29:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:29:32 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:29:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:29:32 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:29:32 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:29:32 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 17:29:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 17:29:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:29:35 GMT
USER gradle
# Fri, 03 Apr 2026 17:29:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 17:29:35 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429711ba4253426e63ee61f0328e01ea895f7d5cae97ca247ad3ab091625ab5c`  
		Last Modified: Fri, 03 Apr 2026 17:15:45 GMT  
		Size: 155.7 MB (155727752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5100319b7e379de94fcd2b5f5e7f5bbae53f3204c6205e01939acb86300a0e68`  
		Last Modified: Fri, 03 Apr 2026 17:30:06 GMT  
		Size: 85.5 MB (85545614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32124735d1386f6ba5980c4c292cd9bdef36238404eab953ca5fd61874969ed`  
		Last Modified: Fri, 03 Apr 2026 17:30:02 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409d9b92ec9f6a18257249f74a4bf0e55c00837a5b526506deee366eb93e30eb`  
		Last Modified: Fri, 03 Apr 2026 17:30:07 GMT  
		Size: 137.4 MB (137388272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96d6965ac14c238e2a67464f3dca34aa5c35ec40f0b913585d7610007a1e263`  
		Last Modified: Fri, 03 Apr 2026 17:30:02 GMT  
		Size: 59.5 KB (59518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:5aa74ae4af22d6f718251de5e8a115cea6dfde42ce92652d0db4f690e7bd6d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00706b669961c616e486a682492879d429bfdb86ead2f2a309242c5675a8037`

```dockerfile
```

-	Layers:
	-	`sha256:06492ef8d0df1e5b066bc231fb53301c1cd6be5502ee84266eb1626d69ae0294`  
		Last Modified: Fri, 03 Apr 2026 17:30:03 GMT  
		Size: 11.3 MB (11338904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58ef2a08f13b15a3325f0d0ea9e408c57305e4c5881d0a2e4e9c3358e31fa75d`  
		Last Modified: Fri, 03 Apr 2026 17:30:02 GMT  
		Size: 20.9 KB (20900 bytes)  
		MIME: application/vnd.in-toto+json
