## `gradle:9-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:4fd1ca0283965b826737fe45ad00f78b132ffda4c73b1cb761e2e85f5dd1c5aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:3f499ae4417a266245dc6c28e79d8560b39ff84a7d8ada9ed703c08ec3908878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.0 MB (438995958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a74da625e2a56ac858d37633ddcdaca0730ff58d9f7f66185df3f1fca15c043`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:06 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:05:06 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:06 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:06 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 29 Jun 2026 17:13:27 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:28 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:28 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:28 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:30 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:30 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123c983efb3d9caab78dd5f7e804d4131aca7970c4f8c80cdc377a8fc76a1809`  
		Last Modified: Mon, 22 Jun 2026 18:05:28 GMT  
		Size: 157.2 MB (157157640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c7f899e4b9df870a2a859cc0aebd77695c8a03d65d65be832b378766ca1430`  
		Last Modified: Mon, 29 Jun 2026 17:14:04 GMT  
		Size: 86.6 MB (86640831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a1682bec8d9fd62066401b132b0eb76f151c639d9bbe50143fedd318691a1e`  
		Last Modified: Mon, 29 Jun 2026 17:13:58 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f964c6bd71153e28cac4b71033b8760264572891cd91f7e7e218389c1c5cf3`  
		Last Modified: Mon, 29 Jun 2026 17:14:06 GMT  
		Size: 140.6 MB (140596022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85ab35dea9591916edbd0913a6f62c528e068fbecf9788ef67d39b534592573`  
		Last Modified: Mon, 29 Jun 2026 17:13:58 GMT  
		Size: 25.6 KB (25603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b08e5fd8a799975b8acf0b3aa62b23b17b6b3db53032845213129bfd40e5ee50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11404129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9925a75f09c0b1f07b2844f7d96b505c0685b74eb1ab427c0c5567598e2dacd0`

```dockerfile
```

-	Layers:
	-	`sha256:9a6db67e37af12c3bb1af660ec817145c060a6e7c7d7fedc49d5f68ee26520a6`  
		Last Modified: Mon, 29 Jun 2026 17:13:59 GMT  
		Size: 11.4 MB (11382633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056560b707054bfe54bd64cd8ad417a27b12d380f8ae323ff5b6f848b300b07f`  
		Last Modified: Mon, 29 Jun 2026 17:13:58 GMT  
		Size: 21.5 KB (21496 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2cf317c9a86471b40b8c64641ea96213bfe3b73b8277c87d12ed2dd703bf584e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.1 MB (436100682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da64e5c3c1d71f3dbe1281996712835996bbe7e27ad14f4c11beb9a488f0997`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:43 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:14:43 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:14:43 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:14:43 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 29 Jun 2026 17:13:09 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:13:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:13:09 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:13:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:13:09 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:13:09 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:13:09 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:13:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:13:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:13:12 GMT
USER gradle
# Mon, 29 Jun 2026 17:13:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:13:12 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e6827a1bd934536bbaca8ee73b82a907a6f504f2a8c7bf2da0903d11d72d4b`  
		Last Modified: Mon, 22 Jun 2026 18:15:06 GMT  
		Size: 156.0 MB (155988813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91534f0d6aaa5ddb21433d3acad2fc52a146a59db5506fdddf340c4c9deb5e9e`  
		Last Modified: Mon, 29 Jun 2026 17:13:44 GMT  
		Size: 86.0 MB (86034157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c10278c04f0c6c11f05e04629c9f72d5155d1437bd6ee4f372b8e8e68102a52`  
		Last Modified: Mon, 29 Jun 2026 17:13:40 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e151075ce7a28072e5a38caa2d025de6e4d28584bc03538506e0c63cc076caf`  
		Last Modified: Mon, 29 Jun 2026 17:13:45 GMT  
		Size: 140.6 MB (140596024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98a4b02caee12bd17973ada7b9ed61c239d40808ffb9abf60875e54c2db7961`  
		Last Modified: Mon, 29 Jun 2026 17:13:40 GMT  
		Size: 29.3 KB (29325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:1e6ecec3974a4f48121b14022117cdb2c3792cd1636269cde0d0dda1cef183ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11403327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109c4142eaaa625dbb64550492c699dc7f1fb86565afbeed3a8f0f9ddaf9580f`

```dockerfile
```

-	Layers:
	-	`sha256:7df2f67e08f4006d91277829b0afd758e4e91b025a983a98e607a052ab32d188`  
		Last Modified: Mon, 29 Jun 2026 17:13:41 GMT  
		Size: 11.4 MB (11381633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:926e538f4577295545980f18702ceaa17922f28ee00a86554b7eb163abf4ca40`  
		Last Modified: Mon, 29 Jun 2026 17:13:40 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
