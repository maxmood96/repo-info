## `gradle:8-jdk17-corretto`

```console
$ docker pull gradle@sha256:1673bdeae68e4104e717d47a436ad889e9c2759fb89b28ad2c401bc48f71bcbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:2532e13adae98dfc50481ee72dd2b47f7b75bd205ce9dfabbaac24ae34a34644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.3 MB (435323256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9ea2f71646943f08aee825725acbd9bd8c94a02a4271dd987a3af7347422f2`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:12:23 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:12:23 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:12:23 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:12:23 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:12:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 24 Apr 2026 01:11:39 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:11:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:11:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:11:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:11:40 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:11:40 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:11:40 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 24 Apr 2026 01:11:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 24 Apr 2026 01:11:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:11:43 GMT
USER gradle
# Fri, 24 Apr 2026 01:11:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:11:43 GMT
USER root
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477e9f05faae959d6f84685f2d7a1a34f252a50c991cef521592fa0ba7eb6e19`  
		Last Modified: Fri, 24 Apr 2026 00:12:45 GMT  
		Size: 157.2 MB (157155286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4845579f8fedd1464343f882aee74971f10ff1f91f8268ca1a5ff27f546be4bf`  
		Last Modified: Fri, 24 Apr 2026 01:12:14 GMT  
		Size: 86.2 MB (86153430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ae14689941ca3397efae02c24808009acbbd6d1954af520701402c020395ca`  
		Last Modified: Fri, 24 Apr 2026 01:12:10 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7320562aac6f7e4a9e82e3120ca871d81381f684aa8029a1e2ad1c7d0b359b`  
		Last Modified: Fri, 24 Apr 2026 01:12:15 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6fc2dc32e47a7d4897891daaea815e28e9d0d248f243596e566b83aea789c4`  
		Last Modified: Fri, 24 Apr 2026 01:12:11 GMT  
		Size: 54.9 KB (54889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7e75565c715dbbb454321e78f292033c18bf9d1dff3294e524308196d761f670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbe5412157b4003a90f6617c5d8f778c9892a0661250c01b6b7af6780b83b20`

```dockerfile
```

-	Layers:
	-	`sha256:71f5ca662b98bbc057df357b288b73481226d7a212d3ea628e3463a0ff04bcd9`  
		Last Modified: Fri, 24 Apr 2026 01:12:11 GMT  
		Size: 11.4 MB (11350170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28135e6e6bf0b30d71748ab62e37dba58d6a9f9f0e1f21ae5460aaa6136e3d49`  
		Last Modified: Fri, 24 Apr 2026 01:12:11 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d1972df1536161c2d3f6626248d7d50556e0b40fa8a0e477b89404795a4dcb07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.5 MB (432546601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9765a61696c35376935f7660a03cb10b3f46f55a504ea80dca494d8e51b5689`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:11:41 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:11:41 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:11:41 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:11:41 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:11:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 24 Apr 2026 01:11:39 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:11:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:11:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:11:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:11:39 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:11:40 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:11:40 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 24 Apr 2026 01:11:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 24 Apr 2026 01:11:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:11:42 GMT
USER gradle
# Fri, 24 Apr 2026 01:11:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 24 Apr 2026 01:11:43 GMT
USER root
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19190c1206066bd46b5a1a6031fd9b5849728dcd0c5a9c3b3c243071f3d9160`  
		Last Modified: Fri, 24 Apr 2026 00:12:03 GMT  
		Size: 156.0 MB (155987864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bae3e596eacaf45d97fe265f6330da9ce282945263e08d0f2470ab633a1298f`  
		Last Modified: Fri, 24 Apr 2026 01:12:14 GMT  
		Size: 85.7 MB (85657022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8cabdd3e819c0eb05c5dd8352344ce3890c2a88e6f060894e116bea110a292`  
		Last Modified: Fri, 24 Apr 2026 01:12:10 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b64473a8385a74f8bd493245b5637a005b570eb8e046ca0e713c8a94ff2f12`  
		Last Modified: Fri, 24 Apr 2026 01:12:15 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdec6434b97d60a1d81f194607c6cdd50b0b124a964ac7388dea7cc692292ddc`  
		Last Modified: Fri, 24 Apr 2026 01:12:11 GMT  
		Size: 59.5 KB (59516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:6a8a98c0c6550ce9a82b91841459a0faba138fd0d11a6ae201123fc1b813e904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8ab1bbcd2951ca5caf0ab110925cccac5c0bbb5beddf89aaf603356976f4f1`

```dockerfile
```

-	Layers:
	-	`sha256:65eae4e8463cf664cc82a3ae809cf68a6af99ae8d812a54d154ec1bc62d51f79`  
		Last Modified: Fri, 24 Apr 2026 01:12:11 GMT  
		Size: 11.3 MB (11349146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff153eff81a14fc286da6241a0dd00a318ce9372a01f8abbe059a4c7a656aba1`  
		Last Modified: Fri, 24 Apr 2026 01:12:10 GMT  
		Size: 20.9 KB (20900 bytes)  
		MIME: application/vnd.in-toto+json
