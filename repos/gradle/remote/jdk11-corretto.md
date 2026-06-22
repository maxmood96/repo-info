## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:4857bdbcb6522347d9ac1cf6b42514396ad5690f27565d4d0088e56faa2d3273
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:81d45961e325e13c25d2db43079bf663696ba10c6e45b9d9c355326edd65e7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.8 MB (432818681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1bb47545832c8e5fa5392f4b86da32aa54f9cccbf3be376e4ba64bcca244eb`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:03:18 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:03:18 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:03:18 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:03:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 22 Jun 2026 18:15:31 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:15:31 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:15:31 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:15:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:15:31 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:15:31 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:15:31 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 22 Jun 2026 18:15:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 22 Jun 2026 18:15:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:15:34 GMT
USER gradle
# Mon, 22 Jun 2026 18:15:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:15:34 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b86e893760418631bb758ba7596a4f62c94cb9b2a50a89142f128dcddcf769`  
		Last Modified: Mon, 22 Jun 2026 18:03:40 GMT  
		Size: 153.5 MB (153472915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5679b296c9c6f681ae481dd3036b6757d5086d659c981902c95be661ea0945f`  
		Last Modified: Mon, 22 Jun 2026 18:16:04 GMT  
		Size: 86.6 MB (86646449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0931ca290891a8be40388cea929a0e91f2f15fd101cf7c88eea67a39e9e3f9`  
		Last Modified: Mon, 22 Jun 2026 18:16:01 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bcf0fabb2dd40589ff0cc5bba2a0e10ca6778d1b808298f25d37a822e5edc1`  
		Last Modified: Mon, 22 Jun 2026 18:16:05 GMT  
		Size: 138.1 MB (138068557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03f9f4581076d4cbfa5c82b520a6fafb5157cf062b8bf4759d7a2b2bf277ddb`  
		Last Modified: Mon, 22 Jun 2026 18:16:01 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:538d72468700113ed1ba30dfacb707c855ee1485b581bb1c02bb61d19ad9c8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11402472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209438f46cefbfe57451e0a92bfa0a0db0a42593c9676656ccca228d07692377`

```dockerfile
```

-	Layers:
	-	`sha256:7efd8be8359f1d4f3f854db9240b7e740033a0ac12a46cb7744ccb1f7db5ade3`  
		Last Modified: Mon, 22 Jun 2026 18:16:01 GMT  
		Size: 11.4 MB (11380808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a612088bf70d3c99b2bdcd8ffb80cf165a2d64f7532e18ca43ae67ed636ba2`  
		Last Modified: Mon, 22 Jun 2026 18:16:01 GMT  
		Size: 21.7 KB (21664 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:fc05362887c1f8a9d223b8bdbf157257ee385b76ecf1818b63829edde17ff323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.7 MB (429667362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa52d38f4704cf8ea297b943fd193d3ce4476f93ef36354e88a799bc00ed41f`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:10 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:14:10 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:14:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 22 Jun 2026 18:28:28 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:28:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:28:28 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:28:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:28:28 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:28:28 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:28:28 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 22 Jun 2026 18:28:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 22 Jun 2026 18:28:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:28:31 GMT
USER gradle
# Mon, 22 Jun 2026 18:28:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:28:31 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde251e78ae931471e2eec1d6090d2888ad7ce776de98251a52827dff5f3dba`  
		Last Modified: Mon, 22 Jun 2026 18:14:31 GMT  
		Size: 152.1 MB (152050355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f699f3082be0815fe10a8633fab3b842f1a64f82d8ac9fa2f40e86dbeeda0a`  
		Last Modified: Mon, 22 Jun 2026 18:29:03 GMT  
		Size: 86.0 MB (86036569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a510cc8c03da9255c2e715a48055f2617b6ad01333c7dc91aeaa6425ce2701c`  
		Last Modified: Mon, 22 Jun 2026 18:29:00 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7389c1d187ce8f3e6ee79542e019d905d4f535a8ef11e49625c31f9a44b047`  
		Last Modified: Mon, 22 Jun 2026 18:29:06 GMT  
		Size: 138.1 MB (138068544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33f171f4febf1ca33c4ab71911f43b0b99a9895f76753687cad286343ea32af`  
		Last Modified: Mon, 22 Jun 2026 18:29:00 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:064de70e58e1bd81acd596aa7090b738775c4b6d48329d25e1538c46048c2054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11402513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7375e0ffb4543011b7fc5c3ecbbb4db2fc247230e8d464e60a058bc0e0be89f`

```dockerfile
```

-	Layers:
	-	`sha256:944c0cac8a72838da8f5c7359d9228122df0a9d020520e1a866150c774282125`  
		Last Modified: Mon, 22 Jun 2026 18:29:00 GMT  
		Size: 11.4 MB (11380651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e3c3e43be8ad7c77f1b15797834acc63bbcacf94ee56e92e2678d8a7a70f8bd`  
		Last Modified: Mon, 22 Jun 2026 18:29:00 GMT  
		Size: 21.9 KB (21862 bytes)  
		MIME: application/vnd.in-toto+json
