## `gradle:9-jdk25-corretto`

```console
$ docker pull gradle@sha256:b62fd204815b385f123d43384c928b54ac7760fe940b79bb5b3df7a5437df88d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:7d9e8da37a8ec1c7bc2ddcf2651c816198d1287e7c04bb70db8856eb6310efb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464710466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7e60fe734cd7d14ca21726bd49b40892f0575b34749cd9ab4bde2dbfd8e94f`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:47 GMT
ARG version=25.0.1.9-1
# Wed, 03 Dec 2025 20:24:47 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:24:47 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:24:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 03 Dec 2025 21:11:42 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:11:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:11:42 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:11:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:11:42 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:11:42 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:11:42 GMT
ENV GRADLE_VERSION=9.2.1
# Wed, 03 Dec 2025 21:11:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Wed, 03 Dec 2025 21:11:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:11:44 GMT
USER gradle
# Wed, 03 Dec 2025 21:11:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 03 Dec 2025 21:11:45 GMT
USER root
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09f7f2c819e1590f71223504205c7a86e2d9ff87d7125644a0f3c3127a36856`  
		Last Modified: Wed, 03 Dec 2025 21:11:12 GMT  
		Size: 189.1 MB (189136572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84309dc9502f244bd5a4012ba7da237f4afbb7ce0c25d372145bbf6c816f3aa1`  
		Last Modified: Wed, 03 Dec 2025 21:12:29 GMT  
		Size: 86.0 MB (86026321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3807297eef039450f041511a2616c38c93a93e499d328de89cf9a43cbe2c5234`  
		Last Modified: Wed, 03 Dec 2025 21:12:21 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be0ee3e2649476ede329dcae6eed47bc45730ac44bc5fc46545a1ee157e0cde`  
		Last Modified: Thu, 04 Dec 2025 01:02:47 GMT  
		Size: 135.5 MB (135521966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762f7277838f6888da4f19500c983b10ba5bfa8580483250ac69d0e574df3f35`  
		Last Modified: Wed, 03 Dec 2025 21:12:22 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c2066bafe0b71c0acae15b6501e409d9413f42ae31cd471bf965523623b3d9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9168a683cd21cfce47b9db2b2cb50ec97c2258cd8f9fa2870593a4b6bd1fbeda`

```dockerfile
```

-	Layers:
	-	`sha256:3fc0617e122560d5cc55a2abbf626d3848f28bccfb3de12f556b5774eb123422`  
		Last Modified: Thu, 04 Dec 2025 00:24:03 GMT  
		Size: 11.3 MB (11349325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e9738ae5ef2d792b6884b0b26178cae800c5b638e8fa73164a46d5ca237ffb`  
		Last Modified: Thu, 04 Dec 2025 00:24:04 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3ce31a0c271636cae22e3a2ee7d6ed1a439cb1036b9406e2189f3e23d5e0fd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461036925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6aced5293b73d99fb6751dadcf2aa5be7bd2c20145f69d74eda57a260b7e7a`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:28:41 GMT
ARG version=25.0.1.9-1
# Wed, 03 Dec 2025 20:28:41 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:28:41 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:28:41 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:28:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 03 Dec 2025 21:12:44 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:12:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:12:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:12:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:12:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:12:44 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:12:44 GMT
ENV GRADLE_VERSION=9.2.1
# Wed, 03 Dec 2025 21:12:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Wed, 03 Dec 2025 21:12:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:12:47 GMT
USER gradle
# Wed, 03 Dec 2025 21:12:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 03 Dec 2025 21:12:47 GMT
USER root
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9fa685c3822bb189356da1a9b3028f8b94634689861f3c390e3231f6f543b`  
		Last Modified: Wed, 03 Dec 2025 21:12:18 GMT  
		Size: 187.1 MB (187059689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2617763a4b06c4426e42b5121c8059655cf7b0d92b415d11529031f7a3c5ffc8`  
		Last Modified: Wed, 03 Dec 2025 21:13:31 GMT  
		Size: 85.5 MB (85524637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1161149c877a2310c8e8c705b081c506028f9c2dbece1787ae821239456140`  
		Last Modified: Wed, 03 Dec 2025 21:13:24 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04eb27e98a3b26018f859a91418702b8f557a7de21dc679c0c317393bfce2faf`  
		Last Modified: Thu, 04 Dec 2025 01:33:18 GMT  
		Size: 135.5 MB (135521967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda610b054d4cd76e4e64ae22856bb108cd152ae55c84002c7a5f58a33d4c23c`  
		Last Modified: Wed, 03 Dec 2025 21:13:24 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:942d67f64d8433b9502f98b014025e54c37ebc69a547cbe322d10c3788b92483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826b40cbe8cc4ce0ad7ad249f62c722b785291c1c4a0a8c3c32837eb6e2b43e2`

```dockerfile
```

-	Layers:
	-	`sha256:6c869ab3b35b2edb159b2bc17b735253bb40fa7048b831f65308e2c69d45b3e9`  
		Last Modified: Thu, 04 Dec 2025 00:24:11 GMT  
		Size: 11.3 MB (11348362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880950c816f4262247830a2fe0d6b7c82fc0454e3d9cd5ea6850eac6cfb38113`  
		Last Modified: Thu, 04 Dec 2025 00:24:12 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
