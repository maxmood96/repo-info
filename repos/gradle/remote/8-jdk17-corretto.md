## `gradle:8-jdk17-corretto`

```console
$ docker pull gradle@sha256:6d355048a9735c2664c77ea26a03967448197c103c811c9efe02cc0cc435d63c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:6db46735ccbc2a6956b823d38a2480eaa7a5ddf95092080ce3822c4b4f357038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413601304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e50c0d6de177ebd4eb9977b849c5173dbf9bae192e42a47931aedc89233c975`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 06 Nov 2024 04:13:47 GMT
CMD ["gradle"]
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Nov 2024 04:13:47 GMT
WORKDIR /home/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 06 Nov 2024 04:13:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER gradle
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a48fc8146362dc325fd39a63dba270fed2777bc9fc1a77be5ac4fb71b413fd1`  
		Last Modified: Mon, 21 Oct 2024 18:57:02 GMT  
		Size: 153.8 MB (153833015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358e689fac34f0fb8a5615891dab46b327952c550b8a03960f90bef3e44594ce`  
		Last Modified: Wed, 06 Nov 2024 20:18:17 GMT  
		Size: 70.6 MB (70638148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb55994a393607954bcf54d4a68543f3282d26064f15403fd68b28dfa56149c9`  
		Last Modified: Wed, 06 Nov 2024 20:18:14 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6a4b9dfcbb193ef6d00fea68d1ed35aad4b087e25f4a431d038b7c1fee81ac`  
		Last Modified: Wed, 06 Nov 2024 20:18:19 GMT  
		Size: 136.7 MB (136729718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11472d63f25de625fede012a113d4cbfa7f4022b47c3bdbda8358d6d1db5ed15`  
		Last Modified: Wed, 06 Nov 2024 20:18:15 GMT  
		Size: 54.9 KB (54913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7c17b56ca8cc14ee64267bbcd66c9e5a67d9724c7c0fbb35376da864761aa9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10781412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0fa2854547bb32651a7d274b3f4bf3fbdcb3d501d66609e67086fdcd556e04`

```dockerfile
```

-	Layers:
	-	`sha256:0db184e99383b914a07de27b7c171790a8e37fa78d811801454cf6f7dfdb8dc6`  
		Last Modified: Wed, 06 Nov 2024 20:18:15 GMT  
		Size: 10.8 MB (10758879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20edfb900287743e086c1bded3475c95c35c1e962aa5e311383acb4f52863809`  
		Last Modified: Wed, 06 Nov 2024 20:18:15 GMT  
		Size: 22.5 KB (22533 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:72e428e70e1b6c3bc75f29c0053352237467d2b90e87cb7e813f775cc4ccf157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 MB (410902209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190ebd6fa49cdcf8bac3564e40c1efc722b6f2bd83113491551b4bb99b11581f`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 06 Nov 2024 04:13:47 GMT
CMD ["gradle"]
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Nov 2024 04:13:47 GMT
WORKDIR /home/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 06 Nov 2024 04:13:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER gradle
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:ec188ec9ab67d19829a9f75d24a165b6b31e1c611a03fdfabfdf4f1950a2c30a`  
		Last Modified: Wed, 06 Nov 2024 22:31:41 GMT  
		Size: 51.4 MB (51424001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaedc9f5ce28005dd055184d5954209a3d1780c746cd2aa5b087b9cac3ab72e`  
		Last Modified: Thu, 07 Nov 2024 21:51:54 GMT  
		Size: 152.3 MB (152335894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdafa4c56fa7eb1b385efab39e2a4d20669d11e835c4d143594253f969d61686`  
		Last Modified: Thu, 07 Nov 2024 22:50:12 GMT  
		Size: 70.4 MB (70351369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db78c746e97ed5fc87420a0be170ef487dcc207dcad28e75b3e363644863dc10`  
		Last Modified: Thu, 07 Nov 2024 22:50:10 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c05381f22f0774ce549871856bf3a89cf20d90fdca1c60dd1f795e30e75f574`  
		Last Modified: Thu, 07 Nov 2024 22:50:14 GMT  
		Size: 136.7 MB (136729734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c8fce11e396bdfec544ce36a344d43b9237c32f501acfb1816ffd0268d0f3a`  
		Last Modified: Thu, 07 Nov 2024 22:50:11 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:9fba159258aeb1c94a6718bd46a0384c1fbe2f7d0b2f3ee862ec616e4e8ba3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10781621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b436d2abb76d56d7f38d7efc137061ea366c95fd2d486848593941b49186aa56`

```dockerfile
```

-	Layers:
	-	`sha256:bda0c25d0cd759c88ae99f74d676ae4465d7f7f6c733b4578de48c0d3c7965ce`  
		Last Modified: Thu, 07 Nov 2024 22:50:11 GMT  
		Size: 10.8 MB (10758795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88405820565dca46bcec77683baeb6c5d60e17ec0a1afb7fd7594cb239f2952a`  
		Last Modified: Thu, 07 Nov 2024 22:50:10 GMT  
		Size: 22.8 KB (22826 bytes)  
		MIME: application/vnd.in-toto+json
