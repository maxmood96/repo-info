## `gradle:9-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:8db8cadeccf6ddb2ecf0f166dca9f947e47d7dde285107635292297525843b62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:5fa0cd6b85f062058df2a810d7a052026e1e5263330f8c874f94192898cf062b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.7 MB (435713893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56825203b1006d64d60b46774dd2797a2ee2b0124c68071f7b45f97b91426243`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:12:23 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:12:23 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:12:23 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:12:23 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:12:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 24 Apr 2026 01:11:23 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:11:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:11:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:11:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:11:23 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:11:23 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:11:23 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 24 Apr 2026 01:11:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 24 Apr 2026 01:11:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:11:26 GMT
USER gradle
# Fri, 24 Apr 2026 01:11:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 24 Apr 2026 01:11:27 GMT
USER root
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477e9f05faae959d6f84685f2d7a1a34f252a50c991cef521592fa0ba7eb6e19`  
		Last Modified: Fri, 24 Apr 2026 00:12:45 GMT  
		Size: 157.2 MB (157155286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e647193f3582d6a1d12866ea691091d2ac12e9b35bf41a0ffccaea54cf6c0a6d`  
		Last Modified: Fri, 24 Apr 2026 01:11:57 GMT  
		Size: 86.2 MB (86153270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8aadf4b3ab13c88eadb51e76d3543ca44e3fcf828464e1dca1a4920f24c51d`  
		Last Modified: Fri, 24 Apr 2026 01:11:54 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2a41abf6a186620e119edc9f7de5bd91cd472dde7afaa061509fae566d753d`  
		Last Modified: Fri, 24 Apr 2026 01:11:58 GMT  
		Size: 137.8 MB (137808333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb9a0bd164a6b994fc104e2ef63a3b3a36646856e3da0e3a98fef2d325ac7ef`  
		Last Modified: Fri, 24 Apr 2026 01:11:54 GMT  
		Size: 25.6 KB (25619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:be5cbe5b2fec217b57284addda2df858638a5b7c5dd48853a5887ba8bf479f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3103ca77b2b5475260a1d4bd6cbc2b92181b3664c9a311a7ae593979b6cb6ce5`

```dockerfile
```

-	Layers:
	-	`sha256:ea1f30c652ad2a48730daf8ff217c78d74aaddf34075829adb484677d6130bb9`  
		Last Modified: Fri, 24 Apr 2026 01:11:54 GMT  
		Size: 11.3 MB (11336573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98eb5185f433e3a102761f45c7c4c0c255497cdf1382cbeea39068b5581a88f`  
		Last Modified: Fri, 24 Apr 2026 01:11:54 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7c705cc76493e424b2b20a0c4762f305a16a4718e8a9256a552ccf27d783a826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 MB (432936611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587ebb82ae2e6791b5d525d862a6f9ab16780aa97ec49c54e8e70cbd7c460f78`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:11:41 GMT
ARG version=17.0.19.10-1
# Fri, 24 Apr 2026 00:11:41 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:11:41 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:11:41 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:11:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 24 Apr 2026 01:11:32 GMT
CMD ["gradle"]
# Fri, 24 Apr 2026 01:11:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 24 Apr 2026 01:11:32 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 24 Apr 2026 01:11:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 24 Apr 2026 01:11:32 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 24 Apr 2026 01:11:32 GMT
WORKDIR /home/gradle
# Fri, 24 Apr 2026 01:11:32 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 24 Apr 2026 01:11:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 24 Apr 2026 01:11:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 24 Apr 2026 01:11:35 GMT
USER gradle
# Fri, 24 Apr 2026 01:11:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 24 Apr 2026 01:11:35 GMT
USER root
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19190c1206066bd46b5a1a6031fd9b5849728dcd0c5a9c3b3c243071f3d9160`  
		Last Modified: Fri, 24 Apr 2026 00:12:03 GMT  
		Size: 156.0 MB (155987864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13738f2eca90072f999cd500d3793e21241508a73029917c9a58aa2b674d54c`  
		Last Modified: Fri, 24 Apr 2026 01:12:12 GMT  
		Size: 85.7 MB (85657155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61944092dd96b4085744be854fac4748ab66b995452a2c43672774987ee1d718`  
		Last Modified: Fri, 24 Apr 2026 01:12:03 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f18e6d2377f82250091290b01511f6be0b2a67db96816a81b8d3f56cc3db7f8`  
		Last Modified: Fri, 24 Apr 2026 01:12:08 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071d0ff236dcb7b54a6de032f464c9a7199042552cac5eee7b435d9d09ea27f4`  
		Last Modified: Fri, 24 Apr 2026 01:12:04 GMT  
		Size: 29.3 KB (29327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:52f289207e1d9f7e2fb51c789eb028f2b53e6e8b11b0f00904f0f1ef4f799bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11357267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1476dc74523a56c7043476f5193e765217477fb858c459cc2eedf516d353fe10`

```dockerfile
```

-	Layers:
	-	`sha256:741c8f3835e7d71e332ce5b74f9d24ce834721d9c61d468d1bc269921ea62c10`  
		Last Modified: Fri, 24 Apr 2026 01:12:04 GMT  
		Size: 11.3 MB (11335573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f401f3ddfba8fdc1410c724660a124b0e228f24253725062842ac109218b1a07`  
		Last Modified: Fri, 24 Apr 2026 01:12:04 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
