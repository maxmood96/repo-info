## `gradle:jdk21-corretto`

```console
$ docker pull gradle@sha256:06346c0949f4ca2e5e2691504b63528bc55a5745627259e93686fdcdcb565a07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:f1b293649f54dc1e557a359345e5114176431560b69ae95e40e85b9692d9c9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430192070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9737ba8be402e3710754960837231a234d5fee0fa485a7a531e1a940964d7815`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER gradle
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER root
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7cd1ddb95c1ab4ae8c9a6cb4c02e3f8eb17e4afe0942c11f465c105cedafea`  
		Last Modified: Fri, 20 Dec 2024 22:33:30 GMT  
		Size: 169.8 MB (169755700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdf5c530c1354e8a7ad68fbdfe8179269c36cd3731e7a6657a34e06cd36e5d2`  
		Size: 70.7 MB (70659401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366dc1a3325cde8c3b6bab41db28300ff7cfe6be4330c383a0e61b7c6c489295`  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99ac8dfbd5874daa2ef8b7ffe9dee0db91c97c41fdf88cd4bb1a17a7c73009b`  
		Last Modified: Fri, 20 Dec 2024 23:15:00 GMT  
		Size: 136.6 MB (136564074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f3f6076897b32f4955ea31103e2c8f4450d63e563b797e15f3ddea14d25e1a`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:dbe8cf81b5847525368640fef777dc49a4e0e435c28800355a8943e6aaa7cdd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10741009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de22f891d2a2dff8eff057ee0c62f4e7c2724c3d744e9f28ad5177c24d29de3d`

```dockerfile
```

-	Layers:
	-	`sha256:82c832885b38861c1170ca0328efc3f288b3bc503373054c36340b159263995e`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 10.7 MB (10720490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c0f1f80b85b8ad86e90708f16635d96598a234a6852fe2b876e53f74dd0850`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
		Size: 20.5 KB (20519 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e0cef6e0048c3edec12a4ece6e789f7d82909e07d965f7695557073f94d5c2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.3 MB (427251993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4d4b50658b9d75167c190d375c582beacfe69bb12a1d10adc95351a3890e12`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER gradle
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
USER root
```

-	Layers:
	-	`sha256:98ab3ce9b55607064b358289eeb810db43f69e016067c07e7136a807475f6f27`  
		Last Modified: Tue, 17 Dec 2024 02:01:08 GMT  
		Size: 52.3 MB (52276382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db84ef8cfc88bb6499cbbfc388592064579203e274d484fa2664344223cbade8`  
		Last Modified: Sat, 21 Dec 2024 01:50:26 GMT  
		Size: 168.0 MB (167984965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d810934d60737284133e57e5c8eb6922ff6f9c2112af44d6aebf5f9ff67602c`  
		Last Modified: Sat, 21 Dec 2024 04:35:43 GMT  
		Size: 70.4 MB (70365362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af93247e9e170e3fcc2797d9073682e4a7624500437bf713f2213a5a98e1901b`  
		Last Modified: Sat, 21 Dec 2024 04:35:40 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8044a481403aa2cc44d541c54bdfb5710ae5e3558a6f21f1e78a41b55021c5e2`  
		Last Modified: Sat, 21 Dec 2024 04:35:44 GMT  
		Size: 136.6 MB (136564074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d513031079eb9810e4d6f116136007580c292eb417dbbc4f95cac924c66260`  
		Last Modified: Sat, 21 Dec 2024 04:35:41 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:1bef09a882cb72323aff4c59759d4eef87b5f92b29f54b7d618ec5d6949b3b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf467263cdf52f151279f465ebb55f4dba77a968ef909145054fb07547317a30`

```dockerfile
```

-	Layers:
	-	`sha256:07cbf8ae3c8d37eb61da90a285205782c2e88dfab2e3b8db6c5cf63db6f9929a`  
		Last Modified: Sat, 21 Dec 2024 04:35:41 GMT  
		Size: 10.7 MB (10719516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee542e8d5661de5638da517e873ccc4481f61aba61df0c2547222d67968a482b`  
		Last Modified: Sat, 21 Dec 2024 04:35:40 GMT  
		Size: 20.7 KB (20740 bytes)  
		MIME: application/vnd.in-toto+json
