## `gradle:jdk26-corretto`

```console
$ docker pull gradle@sha256:e8ff2e40094770ac2b004e81b3170facef9a98b4d9e8b6b29cb1e72868803997
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk26-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:b0f7e68cac0c73b0aef7d2d1a2f57980d60e8b209445645a6b8d35cdf968f11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.3 MB (475291076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b6e6d7b98b27edc71becb669c35d6078b96dc7e10768c258f6f927c3c883fe`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:41 GMT
ARG version=26.0.1.8-1
# Mon, 22 Jun 2026 18:05:41 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:41 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:41 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 29 Jun 2026 17:14:19 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:14:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:14:19 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:14:19 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:14:19 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:19 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:21 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:22 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89540e7f1948b9cdfd916831c36aadc51bc055ba3210b16a29c727cca6e3c68`  
		Last Modified: Mon, 22 Jun 2026 18:06:04 GMT  
		Size: 193.4 MB (193449808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31299cce9aaf4cde51e4854497c2106494141f1170a4e6c71cfda4594e9d64ec`  
		Last Modified: Mon, 29 Jun 2026 17:14:54 GMT  
		Size: 86.6 MB (86643820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ebfd99d67f1be440b55cd128e6b08eea70aaeea7331da05eea6ae0db8e99e7`  
		Last Modified: Mon, 29 Jun 2026 17:14:50 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e203405399458a5a74be9a48e5bdf6d059e770eaf076831afa556ec5590907f`  
		Last Modified: Mon, 29 Jun 2026 17:14:56 GMT  
		Size: 140.6 MB (140595969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e9c0937f12aa75ffd34cb3ae71cfe72b1de010d59fb6958538e5aa3f05ca8e`  
		Last Modified: Mon, 29 Jun 2026 17:14:51 GMT  
		Size: 25.6 KB (25615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d08a1fc9547579bb6c276855890dc44134f770825cdcc8238a6bf4f6dfda3ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11414170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1dc3f24ce2e4a28945214b96527f952a6379702c7faf1f70ff46ba95b34da8e`

```dockerfile
```

-	Layers:
	-	`sha256:8acf2625a1b29caa33783733fc0b9d7477e8fae716550567a4278425c21e9827`  
		Last Modified: Mon, 29 Jun 2026 17:14:51 GMT  
		Size: 11.4 MB (11392519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35ec7f5cffcd92e018bae03f537e8f9ceb19dca418755e8c81d5d3a65ca9fc3`  
		Last Modified: Mon, 29 Jun 2026 17:14:51 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f56db21c3aed32c9caeebb68d446958af837c2b5c7c3e60ff2b12f8648400e83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.4 MB (471393556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ea5113fde03f4a2b8208381fe828937e8ef3dbcff92578613e074c89f52ef`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:41 GMT
ARG version=26.0.1.8-1
# Mon, 22 Jun 2026 18:15:41 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:41 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:41 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 29 Jun 2026 17:14:23 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:14:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:14:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:14:23 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:14:23 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:23 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:26 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:26 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d96dfa1bda3810217adf300288ddcf0930ea9cdb2f132ac9d7c70180a735c41`  
		Last Modified: Mon, 22 Jun 2026 18:16:07 GMT  
		Size: 191.3 MB (191273399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd03d65e9f717cf3fd31835a13b7637f08e9958422646bfe4cff63af1adf128`  
		Last Modified: Mon, 29 Jun 2026 17:14:58 GMT  
		Size: 86.0 MB (86042435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd6a17a66f987f6fbaf0b4a59fe43dfa9fa7c4fbdd95e80daa40695842eb6dc`  
		Last Modified: Mon, 29 Jun 2026 17:14:54 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb77d1c31e6e06b2d106d1d4214fa0afc4f10b3ccdb52144c4a71ad24125e14`  
		Last Modified: Mon, 29 Jun 2026 17:14:59 GMT  
		Size: 140.6 MB (140596022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeef4479f119025e48b8dd809fd5d281382f5a4b917066d7a11573ce53bb574`  
		Last Modified: Mon, 29 Jun 2026 17:14:54 GMT  
		Size: 29.3 KB (29337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5dbb32a54c3847f712509a4d4b5f39ca600a5704555c1bc70e7443a27cbf1f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11413376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5237e2a46263bf9b7f20bd5cd4bf7412ad4ee9e9ea1817847c378ddcffc44c`

```dockerfile
```

-	Layers:
	-	`sha256:f60e0a532f856d9c9f8d657867e3d3ebc9f5d07b653978f267de98714ee08ead`  
		Last Modified: Mon, 29 Jun 2026 17:14:55 GMT  
		Size: 11.4 MB (11391528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9ffdefe150d72a9b5267cc9a505eaa24354d1878e0957ab1e5448d921f796bc`  
		Last Modified: Mon, 29 Jun 2026 17:14:54 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
