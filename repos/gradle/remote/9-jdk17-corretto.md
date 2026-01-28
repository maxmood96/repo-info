## `gradle:9-jdk17-corretto`

```console
$ docker pull gradle@sha256:dfa0dc673df0f115f379bb2bf0b5de52779b33fd7ef75fc22d792d210741ef52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:94710ab11c43f0afabe13299a937e98adf45149f0cd79339ac2294bb042db79f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.0 MB (433989251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736913c45821d08d6a875aff319bc8caa6744d8cd7fd010307864d54655fdccd`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:08:04 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:08:04 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:08:04 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:08:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:08:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 28 Jan 2026 04:54:27 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 04:54:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 04:54:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 04:54:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 04:54:27 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 04:54:28 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 04:54:28 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 28 Jan 2026 04:54:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 28 Jan 2026 04:54:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 04:54:30 GMT
USER gradle
# Wed, 28 Jan 2026 04:54:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 28 Jan 2026 04:54:31 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f764ca21eff5f12dc46762e7c29c7efe1ac48c3ad2653b8f68ac3c495c0b82`  
		Last Modified: Wed, 28 Jan 2026 04:08:26 GMT  
		Size: 156.9 MB (156915347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42270fa59d6bee83c68a617e1e5f4d9466bd9fd6ea3382eeab115cf072e92bb`  
		Last Modified: Wed, 28 Jan 2026 04:55:01 GMT  
		Size: 86.0 MB (86033924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dc44f6628bf3d0adc15da4ec24b67e962a45480b9e97c674fb82a4ca80ad75`  
		Last Modified: Wed, 28 Jan 2026 04:54:57 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e60af4c7fe4f9cb515e8127f209e4f28bb0b8eb661f29ea2bbefd0c9298c7f`  
		Last Modified: Wed, 28 Jan 2026 04:55:02 GMT  
		Size: 137.0 MB (136988867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bec7cfdc82147992283e7123cc0ed706ed3f24300baf02c54e6a9e44fd7bb7f`  
		Last Modified: Wed, 28 Jan 2026 04:54:57 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:db9a1fd09731d280efcb700920be5f5a58a299cf7faaa2e759897d3152a5a580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11345193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dcd9b7ee195def717537a9150d24ec09a7d1eec7b9d3a0845e7ddff60eb8642`

```dockerfile
```

-	Layers:
	-	`sha256:7a5f82f869b996026c16baeb67ab63a25c5b509ac8fa2c86f0dc1c7810724d33`  
		Last Modified: Wed, 28 Jan 2026 04:54:58 GMT  
		Size: 11.3 MB (11323696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f752f8597e7af24ce5094c00d64f5b131500e5875646c9c094d532f73603cf47`  
		Last Modified: Wed, 28 Jan 2026 04:54:57 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dab03f680cf0421ef24bae66f6260d0f1bcbeaca4134bf73668df1bf1c491c12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.2 MB (431173431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b138e030b00234bb0ea0467bd9f752010dbae5c650113cacd1572c1786c26e23`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:28:33 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:28:33 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:28:33 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:28:33 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:28:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 28 Jan 2026 05:37:46 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 05:37:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 05:37:46 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 05:37:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 05:37:46 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 05:37:46 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 05:37:46 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 28 Jan 2026 05:37:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 28 Jan 2026 05:37:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 05:37:48 GMT
USER gradle
# Wed, 28 Jan 2026 05:37:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 28 Jan 2026 05:37:49 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0aad64ff72b39223fe7c89c4c32e0df701234a6d10e6450afd2c590b69880b`  
		Last Modified: Wed, 28 Jan 2026 04:28:55 GMT  
		Size: 155.7 MB (155720069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aacd7170565dd8ee78224757e7cd24ef04339c80064a5e402453fec31a4aab`  
		Last Modified: Wed, 28 Jan 2026 05:38:20 GMT  
		Size: 85.5 MB (85516863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f85a2ad17f8bd6a1679407378f4e0d703d4d724dc7212853002c82022aa25f`  
		Last Modified: Wed, 28 Jan 2026 05:38:17 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8ec7fc627de718f870874fa123403f656e8a7ffe50195e0beee181bbf4c4f4`  
		Last Modified: Wed, 28 Jan 2026 05:38:21 GMT  
		Size: 137.0 MB (136988869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f2c5aaa127e69ac39b9f92170346b1eb5ea14977167db3f47d4ebf80a3a161`  
		Last Modified: Wed, 28 Jan 2026 05:38:17 GMT  
		Size: 29.3 KB (29313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:6ee3d466f6b923a607ca8813e7e03c5e6e9278591194fbe4611ff901ad3fc7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11344389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a451761f3cd5272df7058ea71a780ba31f8ad504276f362f83835526283be2c5`

```dockerfile
```

-	Layers:
	-	`sha256:577d7ce44b91a9e1fbf7b4391d2c0d3d8f7c0212a28c73c9a370cfee52a46918`  
		Last Modified: Wed, 28 Jan 2026 05:38:17 GMT  
		Size: 11.3 MB (11322695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1b559748aa1ff0d3a53239c33fe800f5b10d88a6349c444fb5ec5b2b9f41c9`  
		Last Modified: Wed, 28 Jan 2026 05:38:16 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
