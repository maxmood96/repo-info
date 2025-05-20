## `gradle:corretto`

```console
$ docker pull gradle@sha256:bc64a6b3456e12e4f93a9ed52a109f976091d379e2b85c1dc2033b4d0ab6abb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto` - linux; amd64

```console
$ docker pull gradle@sha256:2cf1aff5eb822ff4d49767798442de6669ed5c71ccbe8ccb3ff3298c3211a7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.3 MB (433332146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd30b7673843cbd2ed6c54fd5022481a52bda8c83ea75fd192aeb953813cb21`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
COPY /rootfs/ / # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
ARG version=21.0.7.6-1
# Sat, 26 Apr 2025 01:26:29 GMT
ARG package_version=1
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Wed, 14 May 2025 01:42:44 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1dd26f3fd48ad2bdc7fb164ac55c6714a2039d97013de0c5f2b15de0d74ec1`  
		Last Modified: Mon, 19 May 2025 23:37:14 GMT  
		Size: 169.8 MB (169833486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac2955387d12ce965b43024a4a63a08fdd9d05fa0da935e58624ad74a98c71c`  
		Last Modified: Mon, 19 May 2025 23:46:42 GMT  
		Size: 72.4 MB (72432834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82b3367d4c985a610eec6bfdab3e06fd477c437ce3599da8f5b4d289cfa09c5`  
		Last Modified: Mon, 19 May 2025 23:46:40 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac1080450ff3187dc20ad1b78c910ad88b10054ed372cab74fb46f7c41c2b0`  
		Last Modified: Mon, 19 May 2025 23:46:43 GMT  
		Size: 137.4 MB (137394548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641a2d360d91ecba5951e24a56ae4376b07bae9d24a310ec243a0c2895eefc03`  
		Last Modified: Mon, 19 May 2025 23:46:41 GMT  
		Size: 54.9 KB (54896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:93cfa0eb82d37fbce08d9a901c82a4fbe31cb6d08629a53a8d10c2ad18f2c338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10819827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5599b449fa13d59c550964637568f78e0f1c7273ff3f461e7827e8170e9bd6`

```dockerfile
```

-	Layers:
	-	`sha256:8b80effbd49b347edb5e5ce5c44ada61e76377af843e090be8cc4ff160401870`  
		Last Modified: Mon, 19 May 2025 23:46:41 GMT  
		Size: 10.8 MB (10799308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23be1a90fc9bf0b35da6cb1722a7d657e4b306cd762e1b94c5f4002bf300b637`  
		Last Modified: Mon, 19 May 2025 23:46:41 GMT  
		Size: 20.5 KB (20519 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b41510f5432bcaab9b91ae38485cfccae7e00093577fcacda542d2a5c58cc112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430182920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590ac7d36d9aad3d12979adcc2b1e078efedec658fced4a9e73f65adadaa0066`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
COPY /rootfs/ / # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
ARG version=21.0.7.6-1
# Sat, 26 Apr 2025 01:26:29 GMT
ARG package_version=1
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Wed, 14 May 2025 01:42:43 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd140d5ff7cfeed9c5da7c3591b30e13df8be78b63c8efafddcaf1920a14be7`  
		Last Modified: Tue, 20 May 2025 00:01:28 GMT  
		Size: 168.1 MB (168137719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9f69993c5892ef014b39f6c8fe22e1171f60e1a31d3c3693e3918711201131`  
		Last Modified: Tue, 20 May 2025 00:27:02 GMT  
		Size: 72.0 MB (72023710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172e6620b21d8951095df64aab525fcd65124a887eb0e0407f72d9c1fb5f39cb`  
		Last Modified: Tue, 20 May 2025 00:26:59 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adeefb0872ecab3a23a53a8a06e0cf9b96685aae175fc295a270a13a7978c162`  
		Last Modified: Tue, 20 May 2025 00:27:03 GMT  
		Size: 137.4 MB (137394546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9b3c974ee0f8ca6e20c0499abe4e3a31978d233e4417c7c48449df5a4457e8`  
		Last Modified: Tue, 20 May 2025 00:27:00 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d37c58f6b299446b13e311a27f60a230f9c17bc53c4acab009675a12bb4cada9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10819074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8627ffffc85c1653ba0f2a71a349dadd6ab2b65c56c27e6f26a3dfb18e639b2a`

```dockerfile
```

-	Layers:
	-	`sha256:c3a9cb76bde5353975a32bf54ce6bc084f6ce1276d6342a479307b2656c3bc86`  
		Last Modified: Tue, 20 May 2025 00:27:00 GMT  
		Size: 10.8 MB (10798334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69ff397b06299a0d1e503325b435aae2e52915c9f8b2bed75b3425367ca96c40`  
		Last Modified: Tue, 20 May 2025 00:26:59 GMT  
		Size: 20.7 KB (20740 bytes)  
		MIME: application/vnd.in-toto+json
