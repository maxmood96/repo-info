## `gradle:jdk25-corretto`

```console
$ docker pull gradle@sha256:841ec4c96a2d9581fa8a9c3e4bafad2a5a9d695defca70652fb64b6f1d00115b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:d32400940872f5fed49e07afdb6f906f77e56411d2279431bf0a1d340b243657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464723331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb42954d75cba2aeba16cdf3604e48e8244bac83c0c2140a6226454432a40b4e`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:19:02 GMT
ARG version=25.0.1.9-1
# Thu, 18 Dec 2025 01:19:02 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:19:02 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:19:02 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:19:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 18 Dec 2025 02:18:37 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:18:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:18:37 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:18:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:18:37 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:18:37 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:18:37 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 18 Dec 2025 02:18:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 18 Dec 2025 02:18:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:18:40 GMT
USER gradle
# Thu, 18 Dec 2025 02:18:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 18 Dec 2025 02:18:40 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8303609df13ed58c04373aaef935f0abee11cda5d1f6b342070b4a72fbfc381d`  
		Last Modified: Thu, 18 Dec 2025 01:19:54 GMT  
		Size: 189.1 MB (189138827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd854eedc2dc04d67042224efc220f7c3e3825347e21af7280160314f01b300`  
		Last Modified: Thu, 18 Dec 2025 02:19:26 GMT  
		Size: 86.0 MB (86017493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c548e86bfd2cb626c0c41f85f862580221671fb4f49d217bfc01b0da85779cf4`  
		Last Modified: Thu, 18 Dec 2025 02:19:21 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385b9de12251d5d69466b338798f2989d7cc5d0aebdc11eeb3d0764ee38f3124`  
		Last Modified: Thu, 18 Dec 2025 02:19:55 GMT  
		Size: 135.5 MB (135521970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e275d7b23bd06ba431053f33c74fcbd7674f846116ca08f68f407d3177efb4a2`  
		Last Modified: Thu, 18 Dec 2025 02:19:21 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e09310e398d58906c7098d604956983a843b5082d3c08ea158dc48d50ad67d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f6d93ccc9b99553e0c0cfdd096d460a713dea961084fff4f1e4129a1afacb2`

```dockerfile
```

-	Layers:
	-	`sha256:15cacdd367921e3198c51f9abc6e3147b4aa5fce4bcf74b7b5f65d20f25b1617`  
		Last Modified: Thu, 18 Dec 2025 03:23:09 GMT  
		Size: 11.3 MB (11349337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04098df07697f7e7b06345f81a488b251a0a5718932c13b8038861a94d16e224`  
		Last Modified: Thu, 18 Dec 2025 03:23:10 GMT  
		Size: 22.3 KB (22268 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:55036f51cb12f5151698fe33b07435f22a8ed56c2bbb0d65613335050ac4443d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461039323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482ee16d5e025519d9be93ac5d3cb98097902d5f845263cf2dea3826c58f59bf`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:27:35 GMT
ARG version=25.0.1.9-1
# Thu, 18 Dec 2025 01:27:35 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:27:35 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:27:35 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:27:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 18 Dec 2025 02:19:12 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:12 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:12 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:12 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:12 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 18 Dec 2025 02:19:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 18 Dec 2025 02:19:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:15 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 18 Dec 2025 02:19:15 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612c39deef61a58a025e6feada7d5e61866b65d460e5d2e64f4d258c21076418`  
		Last Modified: Thu, 18 Dec 2025 02:18:45 GMT  
		Size: 187.1 MB (187059395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cfdc15e2d8f0658cde5af781d800c4c5c249b9aba58cdf74b242c690c8a097`  
		Last Modified: Thu, 18 Dec 2025 02:19:59 GMT  
		Size: 85.5 MB (85523305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d012c95d92dda96597a5d4e09bdf6d589a7717c8d4548b73a9ec3c469e78a5`  
		Last Modified: Thu, 18 Dec 2025 02:19:54 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652b0032e41bd4c4ffcb510a7edda58d23fbde3a57680fcb97a5af199b839ba8`  
		Last Modified: Thu, 18 Dec 2025 02:20:19 GMT  
		Size: 135.5 MB (135521965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7186af04b8fd952c9fb7f77c02f3403bd6b905cf59d9c40373bc65522154cb`  
		Last Modified: Thu, 18 Dec 2025 02:19:54 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:285611a3e7a22177c680ae03fc402ffd8ad6b1d674ba068b91b3898aa54ebf5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17f2614669668541da703e55cac1c3f622b5dfd6d29b876b5f32d8c119bf2f9`

```dockerfile
```

-	Layers:
	-	`sha256:94e37d58c659ffb4ed1381c28d1e1de6853636645c7e570027e459d8a2c35820`  
		Last Modified: Thu, 18 Dec 2025 03:23:20 GMT  
		Size: 11.3 MB (11348374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7798e370a878ad8f643c5c52c9d984a82cbee0cf0978e08aed7338d04b8fa2f`  
		Last Modified: Thu, 18 Dec 2025 03:23:21 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
