## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:7b515b9e8c895be6fddd9fedd4d378387362f5b388cee9e9454a3c9e632af1d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:84af518a0d9c7ad70ea211568b7e73226d9aac20a8419de653cc2da4e4d40612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447736856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b519be7df3ea0d49b20a23742a71ca017196b145994c25aac17f5b3aeaf92657`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:44 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:15:44 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:15:44 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:15:44 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 03 Mar 2026 00:12:09 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:12:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:12:09 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:12:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:12:10 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:12:10 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:12:10 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 03 Mar 2026 00:12:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 03 Mar 2026 00:12:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:12:13 GMT
USER gradle
# Tue, 03 Mar 2026 00:12:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:12:13 GMT
USER root
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3206d69860349aa25c9a225b33200274130746ada51655fcd2c5184f817fc0bb`  
		Last Modified: Mon, 02 Mar 2026 23:16:07 GMT  
		Size: 170.2 MB (170191580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f42f7a1061affed9beb602ad9d6d67055342d4e390f7455640dcece7d1e2faa`  
		Last Modified: Tue, 03 Mar 2026 00:12:43 GMT  
		Size: 86.1 MB (86067584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9ada3798f1774103dbb7fac75c40f853b43c7e9eeec189dd8aec233c731c56`  
		Last Modified: Tue, 03 Mar 2026 00:12:39 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185d7e821e8574eb5e751020026fd206fabfd51759b9863f762d241226621fc7`  
		Last Modified: Tue, 03 Mar 2026 00:12:44 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fbf81a5e602d6a4dd4e6657c6982bb3a27c30f5017f0518a027e793aa8cd846`  
		Last Modified: Tue, 03 Mar 2026 00:12:39 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:7a5490a8787e465668a7bc45e78ab5a997e5ef42cf9f49bb488b7da9e9f0467d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884e15f8b0cd921b53c5dad83f1f883df117acdf4b1589cc1a22542aaf88237b`

```dockerfile
```

-	Layers:
	-	`sha256:8ca0229c588e097eb669dce195eed5d3a0446f9f71d9435d3c9fd2128e6e0f79`  
		Last Modified: Tue, 03 Mar 2026 00:12:39 GMT  
		Size: 11.3 MB (11342355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cacea2d079abbc14a9a37f175f77f2d22c5016d36f00b29e5b724e802dfe3855`  
		Last Modified: Tue, 03 Mar 2026 00:12:39 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1efd0ab0b7e62fdd54cd9143f2f2153c39baa3ac021688e00a8bda77aac1968e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.4 MB (444401980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8430d01787157182c8aa737ecb04d720dd7fd8721bd5888c0c12fce5cc65c724`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:15:20 GMT
ARG version=21.0.10.7-1
# Mon, 02 Mar 2026 23:15:20 GMT
ARG package_version=1
# Mon, 02 Mar 2026 23:15:20 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:15:20 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:15:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 03 Mar 2026 00:13:15 GMT
CMD ["gradle"]
# Tue, 03 Mar 2026 00:13:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 03 Mar 2026 00:13:15 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 03 Mar 2026 00:13:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 03 Mar 2026 00:13:16 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 03 Mar 2026 00:13:16 GMT
WORKDIR /home/gradle
# Tue, 03 Mar 2026 00:13:16 GMT
ENV GRADLE_VERSION=8.14.4
# Tue, 03 Mar 2026 00:13:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Tue, 03 Mar 2026 00:13:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 03 Mar 2026 00:13:18 GMT
USER gradle
# Tue, 03 Mar 2026 00:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 03 Mar 2026 00:13:19 GMT
USER root
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d70bc2bd9019cfe8ff01c08bf2c88be35366884c0a91749017cdbe727033a85`  
		Last Modified: Mon, 02 Mar 2026 23:15:44 GMT  
		Size: 168.5 MB (168466634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7010a035ea2a6b531dadc9d7349ce8f39326f4de0df7f00afa99ed031c88064`  
		Last Modified: Tue, 03 Mar 2026 00:13:51 GMT  
		Size: 85.5 MB (85544543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e0cf0d3a7077e7665df980b9c54b59dac64a9ec70967246f188bb1b4b88f6b`  
		Last Modified: Tue, 03 Mar 2026 00:13:47 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d3a04ccc41acbe27ef092c1e61bc843a050402ca3b109a1c5973dfdca54135`  
		Last Modified: Tue, 03 Mar 2026 00:13:52 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c220d1ad739ba4c010000e21928ca2dea1dfe905fa0baa8fbda6df9587fce01`  
		Last Modified: Tue, 03 Mar 2026 00:13:47 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:c5dd7f63135f6349db4013a1082a0189aa59ab04517d210587c6102216746f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11362387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e3aab3cc05849df37a20089e605dba85f8068c4d33b4b69280e5446aeaa89`

```dockerfile
```

-	Layers:
	-	`sha256:a68087201a734a41ee4343b0510b02df95ba60d86884c6025f337f886ed1a008`  
		Last Modified: Tue, 03 Mar 2026 00:13:48 GMT  
		Size: 11.3 MB (11341333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed1897281c7973142b05fce696165135eccff915d94f3b715e4f5e45ef9f55e`  
		Last Modified: Tue, 03 Mar 2026 00:13:47 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
