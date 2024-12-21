## `gradle:corretto-al2023`

```console
$ docker pull gradle@sha256:e50c9842eff576fe5c02978c11442e80d1d01b0c69f38ef33d5621e6b4d45740
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto-al2023` - linux; amd64

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
		Last Modified: Fri, 20 Dec 2024 23:14:59 GMT  
		Size: 70.7 MB (70659401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366dc1a3325cde8c3b6bab41db28300ff7cfe6be4330c383a0e61b7c6c489295`  
		Last Modified: Fri, 20 Dec 2024 23:14:58 GMT  
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

### `gradle:corretto-al2023` - unknown; unknown

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

### `gradle:corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:43931e37315720a11b5d0f05016349d68b1d85704456d39180bd836ce558c21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.7 MB (426739972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8f189c3053227ec14ae399c7ce88a2204a133a56df0b5ce58e477e9dbcd025`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 20 Nov 2024 19:11:06 GMT
CMD ["gradle"]
# Wed, 20 Nov 2024 19:11:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 20 Nov 2024 19:11:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 20 Nov 2024 19:11:06 GMT
WORKDIR /home/gradle
# Wed, 20 Nov 2024 19:11:06 GMT
ENV GRADLE_VERSION=8.11.1
# Wed, 20 Nov 2024 19:11:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=f397b287023acdba1e9f6fc5ea72d22dd63669d59ed4a289a29b1a76eee151c6
# Wed, 20 Nov 2024 19:11:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f397b287023acdba1e9f6fc5ea72d22dd63669d59ed4a289a29b1a76eee151c6
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
USER gradle
# Wed, 20 Nov 2024 19:11:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f397b287023acdba1e9f6fc5ea72d22dd63669d59ed4a289a29b1a76eee151c6
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
USER root
```

-	Layers:
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f38ff443b6dbbe50c39fe5e28664a701d1d9ef37e7260734f9c881393c8908`  
		Last Modified: Mon, 02 Dec 2024 23:28:52 GMT  
		Size: 167.9 MB (167938069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1b1c9e803f1ccd5b131180ac43cbdc27b99e00844875491cf2fe92e98e884`  
		Last Modified: Tue, 03 Dec 2024 00:27:37 GMT  
		Size: 70.4 MB (70359365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b58172ac83873f9698e722381113077bffb2f9bf0b8d15b107286c74b7e90f2`  
		Last Modified: Tue, 03 Dec 2024 00:27:34 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f1a2141e4983b32d551e58ce9e9d96bbfce4183e2c356cdd94147b01fc6697`  
		Last Modified: Tue, 03 Dec 2024 00:27:39 GMT  
		Size: 136.9 MB (136925487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b512e236ba8251da2b93b162515c6185a10927b7e3dae7c00e1e3d4046d90e4`  
		Last Modified: Tue, 03 Dec 2024 00:27:35 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a3b90a32b3049004d98df2890c87bc8a8da4dbafcc83329f6d92ea834b5339e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10764118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8028658324fc1ea9e5c7ea994c86aa706091cd9078dc05ec5118bc6462644b21`

```dockerfile
```

-	Layers:
	-	`sha256:5353a477e7c4251d462ac7f55be3dac02404a20910120a10bb8bdd55ea0bd623`  
		Last Modified: Tue, 03 Dec 2024 00:27:35 GMT  
		Size: 10.7 MB (10743370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff61282af192eed0ebe4eeeb7b02c2937d2d041d8020e60e07965f3cb51cec9`  
		Last Modified: Tue, 03 Dec 2024 00:27:34 GMT  
		Size: 20.7 KB (20748 bytes)  
		MIME: application/vnd.in-toto+json
