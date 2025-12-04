## `gradle:jdk17-corretto`

```console
$ docker pull gradle@sha256:33119197405c537af43e1efdf068f610d03f0f6a50cd128a1cab9406b07a84f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:8c6cbc6dc13c15c77d722c7160ad5d26b3bf7889f4a70ce370c8e55344675fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.5 MB (432460713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b9759df2839c232851e5fd694c653083f846ef90b8c20f6229547b5c4c134d`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:01 GMT
ARG version=17.0.17.10-1
# Wed, 03 Dec 2025 20:24:01 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:24:01 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:24:01 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 03 Dec 2025 21:12:08 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:12:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:12:08 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:12:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:12:09 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:12:09 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:12:09 GMT
ENV GRADLE_VERSION=9.2.1
# Wed, 03 Dec 2025 21:12:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Wed, 03 Dec 2025 21:12:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:12:11 GMT
USER gradle
# Wed, 03 Dec 2025 21:12:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 03 Dec 2025 21:12:11 GMT
USER root
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb42fa1833ca3e0f09e86f4cd62fb19b4c98ee1b5d6e5a383799befc9befce7`  
		Last Modified: Wed, 03 Dec 2025 21:11:48 GMT  
		Size: 156.9 MB (156898456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57114c7a66bfb45e488d60fff44b0fc4220e5f52da1d6ddf269d3fa6e11a49ef`  
		Last Modified: Wed, 03 Dec 2025 21:12:54 GMT  
		Size: 86.0 MB (86014689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5629bf1568ddd405e37b46d2150bcfe3bc15c0e512b27e2ea5e96ef972322e81`  
		Last Modified: Wed, 03 Dec 2025 21:12:49 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e4dd12b4ad3ee7f7061885e5f220eccf1844fed623f1e099fc6be9ccc91178`  
		Last Modified: Thu, 04 Dec 2025 00:26:58 GMT  
		Size: 135.5 MB (135521966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca592bb9250e0dc8c079b7ae277739fdbd91b147cdefbc6737aa9f8fa3dc695d`  
		Last Modified: Wed, 03 Dec 2025 21:12:49 GMT  
		Size: 54.9 KB (54894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0a1f31c8522ed54a8235869e44cf27c7ba036505776ab2104424bf879edde573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11356227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0670f9c7f266b3f44885bf606b37064cb31a2ca40daba6aa1449a301ce0424c1`

```dockerfile
```

-	Layers:
	-	`sha256:b1076757f3cfdef8d6192cc844644bcea36fb1e9a3346d9bf0e5b526ef19c60e`  
		Last Modified: Thu, 04 Dec 2025 00:23:28 GMT  
		Size: 11.3 MB (11334730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f7167ada7f601ecc8c7f1ae642ad95b7ed6cffb3a5f0fd3f6ece423a4a68677`  
		Last Modified: Thu, 04 Dec 2025 00:23:29 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5d46eeb85f33cc84e74dae555e58f20761347568141689f4323dc327998308f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.7 MB (429686519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976e75aea743b9c597bfd0b929067282c4530bebd698aa3ab3b7f87e30b02863`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:28:35 GMT
ARG version=17.0.17.10-1
# Wed, 03 Dec 2025 20:28:35 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:28:35 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:28:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:28:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 03 Dec 2025 21:12:42 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:12:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:12:42 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:12:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:12:42 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:12:42 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:12:42 GMT
ENV GRADLE_VERSION=9.2.1
# Wed, 03 Dec 2025 21:12:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Wed, 03 Dec 2025 21:12:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:12:45 GMT
USER gradle
# Wed, 03 Dec 2025 21:12:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 03 Dec 2025 21:12:45 GMT
USER root
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a016fd9e1e501eb41251ccf29fe4236b2040f1288be81ba13bc093629a8ee72a`  
		Last Modified: Wed, 03 Dec 2025 21:12:15 GMT  
		Size: 155.7 MB (155708073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56c374585bb170fda2698ba84eebb13f988d95f81ff9896b83a1c8aa9c8a8bb`  
		Last Modified: Wed, 03 Dec 2025 21:13:40 GMT  
		Size: 85.5 MB (85525851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e258fca626d42c45aab5915b23b42b662227490d66a3c352cd71a81e69deab09`  
		Last Modified: Wed, 03 Dec 2025 21:13:22 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dfc10e54d014a3093c592aed414bc83b0cb6778e4b2f8c76d8fd99ba78f045`  
		Last Modified: Thu, 04 Dec 2025 00:40:52 GMT  
		Size: 135.5 MB (135521966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b690daac10aa4dfd76e3d662449a938f5eadde78352c8c6d677f91cf1a25c`  
		Last Modified: Wed, 03 Dec 2025 21:13:22 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:9d32d748c83e8fbb99470e8dae0bf6eb916b4ebdf83d474d891fea122dfcaf36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11355422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0676b87d3932648791e16831ec237cd952e91d997e0328ea5c3f3d21d1351e23`

```dockerfile
```

-	Layers:
	-	`sha256:f2a0d90b6213b748906a3a562257383f4d52653a5d1415c9fb9b73ad16e140a7`  
		Last Modified: Thu, 04 Dec 2025 00:23:37 GMT  
		Size: 11.3 MB (11333729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00083fe45aa96d0a0f010cf6842a9f6804ae3482e4aebed167122e0e047de792`  
		Last Modified: Thu, 04 Dec 2025 00:23:38 GMT  
		Size: 21.7 KB (21693 bytes)  
		MIME: application/vnd.in-toto+json
