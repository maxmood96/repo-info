## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:b516fbd17b465d8d3a8b6a91cb71e9fc352946714018b18a320039ba7074a615
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:4a1e2b27ef2d0da192f3fdde9a03c59cb0cf272935d97ce21222d2011b242abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.5 MB (425499386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d3d41872641a13dfc3a718a2e80adf1a737ff9cff37b895a415d351a228f25`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:19 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:11:19 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:11:19 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:11:19 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 27 Jan 2026 23:11:40 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:11:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:11:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:11:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 Jan 2026 23:11:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:11:40 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:11:40 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 27 Jan 2026 23:11:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 27 Jan 2026 23:11:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:11:43 GMT
USER gradle
# Tue, 27 Jan 2026 23:11:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 Jan 2026 23:11:43 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74463adce1e4f57125e9fd9cff6d1ee4e60a88fd9a1be6afad902b0f8a66863a`  
		Last Modified: Tue, 27 Jan 2026 22:11:41 GMT  
		Size: 156.9 MB (156915298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e4e5cd1afd8b07a57a4b0e3dbace0452a5ab38c99c6d304d4f78961a69ceb9`  
		Last Modified: Tue, 27 Jan 2026 23:12:14 GMT  
		Size: 86.0 MB (86034260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46dde66dbf648e4c5a690dc0899e4c9980cbf9ac055b8b844c567d88050e6211`  
		Last Modified: Tue, 27 Jan 2026 23:12:10 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d370cc121d733ea8ae95bb23c91acecb3582817dc2ffbbd4ff664d940a2b1b`  
		Last Modified: Tue, 27 Jan 2026 23:12:15 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b7d4145006d83867cd2ec5407b0e7488f88f09304969cee188949fa6cf2545`  
		Last Modified: Tue, 27 Jan 2026 23:12:10 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:cd7dd85fe9e5e2f33af5fbf78117ccd4bb00578670563c44090b812b0629f309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11271178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9b417efa71e0f6fd02fda936741ac7bbf503ec719d34ae64c0504c181522d3`

```dockerfile
```

-	Layers:
	-	`sha256:c89d9436fef746289f6f70f5fb728ac2eaf738594a7e786a972795d6d28cc688`  
		Last Modified: Tue, 27 Jan 2026 23:12:11 GMT  
		Size: 11.3 MB (11250465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26bd0928b5eb34e43da4a31424a291f9720728fb75f8196aaf71063c77bdff10`  
		Last Modified: Tue, 27 Jan 2026 23:12:10 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d13ba77cd9f47842f5ae03fc399b9feb109728275948316d5d0b6c067139618b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422683733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e9922275762d40b2e55586bd1c873705afeb4146a50535a5182dd173d56db7`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:59 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:11:59 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:11:59 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:11:59 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 27 Jan 2026 23:12:01 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:12:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:12:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:12:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 Jan 2026 23:12:01 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:12:01 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:12:01 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 27 Jan 2026 23:12:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 27 Jan 2026 23:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
USER gradle
# Tue, 27 Jan 2026 23:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2758ef474287296fa6eaf0447f718c4bce08ca792102b09591da08dc54c21b30`  
		Last Modified: Tue, 27 Jan 2026 22:12:22 GMT  
		Size: 155.7 MB (155719962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bddd20573c40c42cad34276935aebd60056dd8a2e19705c6145e21a79f078c`  
		Last Modified: Tue, 27 Jan 2026 23:12:34 GMT  
		Size: 85.5 MB (85516518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c2f6fb26c5dec239857fe4ccbf2ca4e0729b2a494679fd713ef6257d59fc6`  
		Last Modified: Tue, 27 Jan 2026 23:12:31 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd14565b0d0a88bf3e2757b6c6df6f1f2a0964e56f0732717bb05c8c03e52ab`  
		Last Modified: Tue, 27 Jan 2026 23:12:35 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54b964c8354b54c188765a1804d1fe8e307ac499f8eedba75db9012a4914c1a`  
		Last Modified: Tue, 27 Jan 2026 23:12:31 GMT  
		Size: 59.5 KB (59519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:95c2cae00583885b114f2b9274d085c9f744efacb446625bafe68162b7abe50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11270326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5cad00fd30da39f6a9df100ab6d57df3b3fd3a5a76ef1ff7dba2af6d4061cb`

```dockerfile
```

-	Layers:
	-	`sha256:271fb8e8eda6d54fa3f0e00f55963ece53876f817a58239e0a0148e3955ddb7c`  
		Last Modified: Tue, 27 Jan 2026 23:12:32 GMT  
		Size: 11.2 MB (11249440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86163162b9901ada5ebb032c9ad5e0e38a3716c0af85cdd53c6458270ead4d77`  
		Last Modified: Tue, 27 Jan 2026 23:12:31 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
