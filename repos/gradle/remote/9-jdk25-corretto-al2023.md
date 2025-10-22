## `gradle:9-jdk25-corretto-al2023`

```console
$ docker pull gradle@sha256:40d479e02db08b4a53542b3da8d3cf95464c834058899d3863db2ecae4a86cfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:42c7f7226b7e69933ec2417ab5a59ad97458402901905dd3bfb58c38214e8073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.3 MB (463306200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cf429984807fa7fd2c415b044cb6acdcfbe8263275e38cf3df745f191f11d0`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 30 Sep 2025 09:31:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 09:31:25 GMT
ARG version=25.0.1.8-1
# Tue, 30 Sep 2025 09:31:25 GMT
ARG package_version=1
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV LANG=C.UTF-8
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d2c4bebb63b964a5168a7f8dedcb088e3d65ad774c09e8153b520d312ebdb9`  
		Last Modified: Wed, 22 Oct 2025 00:58:29 GMT  
		Size: 189.2 MB (189170547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fba16ff08fb114c176142dd6df220ba6b28a93be9682c87dc8807c1969d787b`  
		Last Modified: Wed, 22 Oct 2025 02:37:54 GMT  
		Size: 85.6 MB (85559257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c8a40ecd2ea6d0ae16337176f4e6c4d8b3f9eee861809629e6e0c5ca161e1a`  
		Last Modified: Wed, 22 Oct 2025 02:37:38 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91d1a5de4ea7d685c52cb55de701fbe873fd849f31a23e92c8c731cbc6fafd7`  
		Last Modified: Wed, 22 Oct 2025 06:29:35 GMT  
		Size: 134.5 MB (134514676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d89888ab88613fb6a94c5cceac9450f95f01d5be8854674acfd5be0bbb66ea`  
		Last Modified: Wed, 22 Oct 2025 02:37:38 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:bc916ae5497b0ab6e97000d55b8d86a9db19882e5d3f70b0a18e14c97c5dafbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11336452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40c99f3f01a50ce62e94e89f899b5959dad055465ec6d29fb40a9ad0bb9b6ca`

```dockerfile
```

-	Layers:
	-	`sha256:1af83c97c139973b50863fbefc035c8f567ba983c9a249f86b49e6a0c57e9f3c`  
		Last Modified: Wed, 22 Oct 2025 05:23:24 GMT  
		Size: 11.3 MB (11314189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44fd270f6229a5ce51dd7e00698c3e61e0f7e6d937e22671fc3b0b69b521e931`  
		Last Modified: Wed, 22 Oct 2025 05:23:25 GMT  
		Size: 22.3 KB (22263 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3f4e4562dad7f6360b2bddc6256033aa8eb9e37a664b31f3e2e010b4b90b7540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.7 MB (459650676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e328e1adf6401efd03f26d3a0c9a701c1bca5942ad18223b18e31bd3bf9b00`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 30 Sep 2025 09:31:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 09:31:25 GMT
ARG version=25.0.1.8-1
# Tue, 30 Sep 2025 09:31:25 GMT
ARG package_version=1
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV LANG=C.UTF-8
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER gradle
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
USER root
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0facfa421fa0d39948514b8fdbe1af18c63525acb19c3f4c8bddc6d0d119af`  
		Last Modified: Tue, 21 Oct 2025 22:11:05 GMT  
		Size: 187.1 MB (187096320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4979421551c57271fbb25c197b8b4ace2a41bc17d9e39d91de0e2fd5711318`  
		Last Modified: Tue, 21 Oct 2025 22:12:45 GMT  
		Size: 85.1 MB (85087200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b85d3c005d6382ef9501d41beb70371287ef59c271823de934b07a13f00bf4`  
		Last Modified: Tue, 21 Oct 2025 22:12:38 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fed172bfc27d1fb0b6f6a491a9fe2a9e61be2d10321d498dc3068b858b79801`  
		Last Modified: Wed, 22 Oct 2025 02:16:12 GMT  
		Size: 134.5 MB (134514744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea16d8c0974efcf7ca9f2513065c5f5e92ed978b37e913bd5296253b7f7ddd2`  
		Last Modified: Tue, 21 Oct 2025 22:12:38 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:f2dd00a509b838a5e2c99563aba1e030c5bff4675c653b9f6a92ef4faccffaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11335710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d1011a7f5603d7ef71c0fb6c1fce85409cab6e9627223bb4167ec97ea005d9`

```dockerfile
```

-	Layers:
	-	`sha256:d2bedd0a958381f4f5e1528c906e5377618ce3703b21e80b06808bd7e2c79a39`  
		Last Modified: Tue, 21 Oct 2025 23:23:44 GMT  
		Size: 11.3 MB (11313226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede9a5f894d532eea77e9f88738878ab91cfc81ad625f2f4a367f41960daa52a`  
		Last Modified: Tue, 21 Oct 2025 23:23:45 GMT  
		Size: 22.5 KB (22484 bytes)  
		MIME: application/vnd.in-toto+json
