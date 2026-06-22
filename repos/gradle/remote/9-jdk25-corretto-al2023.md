## `gradle:9-jdk25-corretto-al2023`

```console
$ docker pull gradle@sha256:22ecbd0be5ed326d981be9c9b84ee1527e61c0ebc6c2ed82eca6c861883f3aa0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:334f34635bc088f83588239fd715a9e369646554acfd375f23acaa6c2a7a984f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.3 MB (471256300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00dd29b14c4659281a29129bf22ec5f079268f526f2f8115b4b796904baf9d6`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:15 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:05:15 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:15 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:15 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 22 Jun 2026 18:15:06 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:15:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:15:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:15:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:15:07 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:15:07 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:15:07 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:15:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:15:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:15:09 GMT
USER gradle
# Mon, 22 Jun 2026 18:15:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:15:10 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9187d1c0652a3fc2e5587c51e615fc4dcfb4ee369050a626cc0c5f8763605ac`  
		Last Modified: Mon, 22 Jun 2026 18:05:41 GMT  
		Size: 189.4 MB (189413466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b347a8a4fbeaa72ed7735335c7f3f085628ad793680ac662c010138ae624761`  
		Last Modified: Mon, 22 Jun 2026 18:15:42 GMT  
		Size: 86.6 MB (86646248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6705f4f8c66f76024ff344359177501d6f0a09fa56725ab53a4cda035aada6`  
		Last Modified: Mon, 22 Jun 2026 18:15:37 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca074b10aaddc8d06cd90c1cd15964da67ff22459d13f1eded99c4acc921f9a4`  
		Last Modified: Mon, 22 Jun 2026 18:15:43 GMT  
		Size: 140.6 MB (140595107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd31746392665c98af0c9f4cfd8f6b333806b74e0b101283f7c4b554a5fdf3`  
		Last Modified: Mon, 22 Jun 2026 18:15:37 GMT  
		Size: 25.6 KB (25615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:828075f279a56273c12fadc085b69baea014d4f770fc0bf63e22c8c70ceb1971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11419497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2555f55018a08e46987972f58b6f13b187328e7c708f7a3438c1c98e1ed82d4`

```dockerfile
```

-	Layers:
	-	`sha256:35188ab2d2add29aa236f671504c1066aa10415092cdfce4779ec38df2eff154`  
		Last Modified: Mon, 22 Jun 2026 18:15:38 GMT  
		Size: 11.4 MB (11397228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d02c888306189c68625d27f4f1ea051f6cce522fee8f9d4268387038c1929e39`  
		Last Modified: Mon, 22 Jun 2026 18:15:37 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:15a63ca215990a43dde73675b2e844c332f79b1e521d0e73a0005aa77bff3d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.4 MB (467442444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35cc4a57dfbd21c9e4e1e568706238f441691852a9a315423bea3a9c65c251c2`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:33 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:15:33 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:33 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 22 Jun 2026 18:25:48 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:25:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:25:48 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:25:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:25:49 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:25:49 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:25:49 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:25:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:25:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:25:51 GMT
USER gradle
# Mon, 22 Jun 2026 18:25:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:25:52 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4f1006a54abcd81b4b8010a4470cc0f1ddc33b2dd4191d1661555e3275be62`  
		Last Modified: Mon, 22 Jun 2026 18:15:59 GMT  
		Size: 187.3 MB (187328296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a825290ec72e2a097600fea204ced21584a06c1d5a82da03dffd7642bb89a3`  
		Last Modified: Mon, 22 Jun 2026 18:26:24 GMT  
		Size: 86.0 MB (86037332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4c3f24249c41e738e1ca9132a1afce3492eef209d7cf2ec6364c74fa03b59e`  
		Last Modified: Mon, 22 Jun 2026 18:26:21 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6932e6987039189a1171a188225962475d99e05fa54e0b4976837d035c9a9fcc`  
		Last Modified: Mon, 22 Jun 2026 18:26:25 GMT  
		Size: 140.6 MB (140595105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531c56b1167aeec5cfc587e38ec2098c190f31a0349c5b1cd2e0abab331cfe23`  
		Last Modified: Mon, 22 Jun 2026 18:26:21 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:70ea35c18076810be5841cf5ebef08c502bd3da9b4319c27350375d65ae033af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11418756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cff92846fe50a721cd5c4db2d6587144c6218443923332ce9936e845586b9a0`

```dockerfile
```

-	Layers:
	-	`sha256:8c0a35d89cc867fd69e50ad900e18814f05f1867e4632daff35398e5f8494989`  
		Last Modified: Mon, 22 Jun 2026 18:26:21 GMT  
		Size: 11.4 MB (11396266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae373f70999852696ff3eeba7393cb94886a39282af5f2163c01b251b5554ad`  
		Last Modified: Mon, 22 Jun 2026 18:26:21 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
