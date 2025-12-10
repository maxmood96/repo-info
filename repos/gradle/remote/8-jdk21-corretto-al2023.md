## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:e75d43c77862d3c985f15a9c3050126c45c52b2654086b7411c5f60914bbf0f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:9a70d88dfd7f8a522c239394de003d665eaa53b24d04ab4959c9ab9addf46343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.6 MB (447628388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7ec3e5685b2f397cb01815b6b8338592ce22b883da88a0bcab03add0153e2e`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:25 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:24:25 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:24:25 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:24:25 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:12:47 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:12:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:12:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:12:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:12:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:12:47 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:12:47 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 03 Dec 2025 21:12:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 03 Dec 2025 21:12:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:12:50 GMT
USER gradle
# Wed, 03 Dec 2025 21:12:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 03 Dec 2025 21:12:50 GMT
USER root
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8cbd3c43733a7e197430ec594b9a379e73c2c0129499a285c897b482d00692`  
		Last Modified: Wed, 03 Dec 2025 21:11:35 GMT  
		Size: 170.2 MB (170185114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7243a033a195806f76695391320aa9164d2d30c6de68b91e1f650f264caa8048`  
		Last Modified: Wed, 03 Dec 2025 21:13:33 GMT  
		Size: 86.0 MB (86022479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8624d9f6dbf427c822e8af5892a4764e57232763633bc1b00420ac62e101201`  
		Last Modified: Wed, 03 Dec 2025 21:13:28 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cabcf74f188dadd65c33987d1dccc52d425af386438f252dd4a1b8d22fd2ce0`  
		Last Modified: Thu, 04 Dec 2025 00:49:24 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65d9035cc52b7f7d4e4a3e7062dba5ba84dc18c350369a958d69e76e55be0b1`  
		Last Modified: Wed, 03 Dec 2025 21:13:28 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:6d78c58682929c3477e5714a5fd0b51cac781d13e53370a08baef69d11a946eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:861e0c64eadfdf92d94d40eac270d831e7398ec7f6ac5fec187255bb3586d592`

```dockerfile
```

-	Layers:
	-	`sha256:9043d0eb332f55ddebeb400b750fb75eafb970699476968426ebb34409a3836b`  
		Last Modified: Thu, 04 Dec 2025 00:21:06 GMT  
		Size: 11.3 MB (11342256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8573e9f355ba39a4113c8da24aab23a5f125130dbc1e71af6428ffe674a409a9`  
		Last Modified: Thu, 04 Dec 2025 00:21:07 GMT  
		Size: 20.9 KB (20880 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:877e3d5b01c6895a03a984e0bfa95af4ce2c308c3687f52021d5eddc353f5678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444295697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4a220404d6132b5f5b617b8643ca4661db1bc789739ab7d7122999c3e1ecbe`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:41 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:27:41 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:27:41 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:27:41 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:11:36 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:11:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:11:36 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:11:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:11:37 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:11:37 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:11:37 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 03 Dec 2025 21:11:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 03 Dec 2025 21:11:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:11:39 GMT
USER gradle
# Wed, 03 Dec 2025 21:11:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 03 Dec 2025 21:11:40 GMT
USER root
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626b53f4a673eb63ba52f6f5686c9b4a1a436ef18af99dc4556d8c58340ae1c5`  
		Last Modified: Wed, 03 Dec 2025 21:10:57 GMT  
		Size: 168.4 MB (168441796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526044e16a5369024459d31321f2c4fe44b8e64154ec1dcb4793d884213d92b5`  
		Last Modified: Wed, 03 Dec 2025 21:12:31 GMT  
		Size: 85.5 MB (85528078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746429d330b717e3ddd992854a5ea5e0857440931c6912a4433a647ce6689d12`  
		Last Modified: Wed, 03 Dec 2025 21:12:21 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac451b12ba936791712d012ddd5259cc9e6464ec9ae122265117b38d61a63d4f`  
		Last Modified: Thu, 04 Dec 2025 00:56:45 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0859f56d80f83381145a7a79c56b1df1b0aac005a80a772880c6ec9d49f074a`  
		Last Modified: Wed, 03 Dec 2025 21:12:21 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:47ac30d233a3002d2e38b633c0f6bac541ed4ef190ccc3e1d8e404aa176c3820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11362288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956239958d6f26a9b9d5dbdc6a8dd1414bb337a1f70cb1488aca138fd6b6701e`

```dockerfile
```

-	Layers:
	-	`sha256:48993aae2cc6febbc2946a94b7b979f8410f3ae253bf36adde30934fe2f4f0a6`  
		Last Modified: Thu, 04 Dec 2025 00:21:16 GMT  
		Size: 11.3 MB (11341234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f860c81a0428f2aaff791599336f9fc699518bd58f34e7604c377f5b8f8965cf`  
		Last Modified: Thu, 04 Dec 2025 00:21:17 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
