## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:e30b5fb5c172a9abacefa2c36d5d1ed8fc9b3c56ae688930f089e22882d00918
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a3b005db3ab2be3ab8b8367ebd5bcf168295ffc293d4d67a7156ea8f2e0b3da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.4 MB (425433852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8076d380342189a0e891d01d8938b276a1e84df314c9a29b9ec2c58bbc5b1d79`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:03 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:18:03 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:18:03 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:18:03 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 18 Dec 2025 02:19:20 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:20 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:20 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:20 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:20 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 18 Dec 2025 02:19:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 18 Dec 2025 02:19:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:23 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:19:23 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c94f0e66ab1ff3543f3fe4f588fab226e2b88a2253456fb47f3f5070963e3f`  
		Last Modified: Thu, 18 Dec 2025 01:18:57 GMT  
		Size: 156.9 MB (156900599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e83dd8449df401f422910c1869643efa271ce35daeda093ad38da389a8a4a30`  
		Last Modified: Thu, 18 Dec 2025 02:20:08 GMT  
		Size: 86.0 MB (86018795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2d4dd3627f0d6cf0dc734cf0bac9e6ab5c3c12f05d0e9d4a7988caf54538c8`  
		Last Modified: Thu, 18 Dec 2025 02:20:00 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6cc7a9612e7bd1622bcd52ca2fa31306dace12c4cbfd49c804933b4335d346d`  
		Last Modified: Thu, 18 Dec 2025 02:20:18 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6c9a07d29ea287f3f619f6b11a9f34abc7d9ac8d67b161f12a398ab227b727`  
		Last Modified: Thu, 18 Dec 2025 02:19:59 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e7a83045af7cc8cb31d64396661188a6684b5a49357593dd4ba94333eb77d938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11271183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b43fa25a3adb14d8531cefa701f56947418f9dc7c43503608c3c80ff82f4ad`

```dockerfile
```

-	Layers:
	-	`sha256:9c36057c9aedb5508194a59491a98d124ab021be696bb3906cd52d1eb59ded4e`  
		Last Modified: Thu, 18 Dec 2025 06:18:43 GMT  
		Size: 11.3 MB (11250471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bc2e5a6560ccf05a9c9cb147de310783a18c80e475bff0daab8f9de1c56c557`  
		Last Modified: Thu, 18 Dec 2025 06:18:44 GMT  
		Size: 20.7 KB (20712 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c378ac59d2f042b198cacec5a11ca3a553e2bbe4350df267a016939b2ad94a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 MB (422633513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976cf5154a7d49a3e6f58a6115f3c481c6a6917bcb81cc367a84b06b9a829b6a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:29 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:26:29 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:26:29 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 18 Dec 2025 02:19:40 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:40 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:40 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:40 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 18 Dec 2025 02:19:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 18 Dec 2025 02:19:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:43 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:19:43 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f9dca445f419513819266ddecf7477b069aa5b3d4e331702639766d5ce2a1`  
		Last Modified: Thu, 18 Dec 2025 01:27:19 GMT  
		Size: 155.7 MB (155707401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e80ab1533f94029b7d135f02439dd34580997c9dd5648ac15d70e0b9805a92f`  
		Last Modified: Thu, 18 Dec 2025 02:20:30 GMT  
		Size: 85.5 MB (85522058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5fd318f8d592999f758bdc74a047bb3376d4f9e6dde79680ac3501687523be7`  
		Last Modified: Thu, 18 Dec 2025 02:20:23 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12caf714cbc91998e1a39bde4cf6dc11112b0432557b82019cf597567d975a2f`  
		Last Modified: Thu, 18 Dec 2025 02:20:41 GMT  
		Size: 128.5 MB (128469413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774ba1640760eae4ff3309900a25cd6cf2a56d659226af84680ab335678f66c4`  
		Last Modified: Thu, 18 Dec 2025 02:20:23 GMT  
		Size: 59.5 KB (59516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:0241fc459ab81f3ad4a52cc724622a7f44580d14789ce6c9f1b8424a032c664f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11270332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b45f67e7c50262de673ed535946f7e5ab767775f72b846a30a6e2a01b47f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:954e7a88f041ece3e70d7640b0f5109d9d3fca8aa52c9d6509cef65a7b076a15`  
		Last Modified: Thu, 18 Dec 2025 03:19:23 GMT  
		Size: 11.2 MB (11249446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b778cfbf8c2e1fb273dc37d5671fafe5a03d91c1d00df1e3f8b1da63154dc5a9`  
		Last Modified: Thu, 18 Dec 2025 03:19:24 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
