## `gradle:jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:df3c3f7a398963376a5835ebe8487d71d75ab69c7c25e002e8d4124c5815b049
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:040c573909b7c2e88152626b32fe1d198d496b4035d85238052ed91777397cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.0 MB (433989136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f4bb7e7707a6c57310840e0ebe8e8ba640965aab3a36b3389188dc304edf94`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:24 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 18:59:24 GMT
ARG package_version=1
# Wed, 21 Jan 2026 18:59:24 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:24 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:13:53 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:13:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:13:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:13:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:13:54 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:13:54 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:13:54 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 21 Jan 2026 19:13:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 21 Jan 2026 19:13:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:13:56 GMT
USER gradle
# Wed, 21 Jan 2026 19:13:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 21 Jan 2026 19:13:56 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9611f4d384734b62e775c9d6504436549d04bb86a1c85fb4d696880e755c9a`  
		Last Modified: Wed, 21 Jan 2026 18:59:47 GMT  
		Size: 156.9 MB (156916086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda0f272c0b30626d825e58916395bcdeb22bdea52962907b5daba46d896aa65`  
		Last Modified: Wed, 21 Jan 2026 21:42:23 GMT  
		Size: 86.0 MB (86035704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0c199a649d6418524edef954343b7cb042033d878318caae9168a930afcdd6`  
		Last Modified: Wed, 21 Jan 2026 19:14:46 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5de32c16c4124d50f5d97fcadda533d8abb9332841eba58a39fe4aa82d2440`  
		Last Modified: Wed, 21 Jan 2026 19:14:26 GMT  
		Size: 137.0 MB (136988869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e2bccb3c5126bc407817b98d71855b12f9cae72ca2d03c4dc0bb18cc3404b2`  
		Last Modified: Wed, 21 Jan 2026 19:14:20 GMT  
		Size: 25.6 KB (25590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b3a6f4eae69e2db79c613806b68f342a16b7344f6afc6b440ed4055b97bbedde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11345193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686ff94a992fec56e8152f437b2b7d8b7595266f4d2d76a213f0006b0fb938a6`

```dockerfile
```

-	Layers:
	-	`sha256:4bf58a23171d5d9ad7ccb5d017c54ac68d606b9fd2ba968d4736de0e9935eac0`  
		Last Modified: Wed, 21 Jan 2026 19:14:21 GMT  
		Size: 11.3 MB (11323696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620016dff7aa872e1ac8dca24a1bf0e30dfceab31548107a8c9781cbd3161b2b`  
		Last Modified: Wed, 21 Jan 2026 19:14:20 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:89c19fccb4de9e47c2e38b83602a7abe0a5de7375555308c06e7f80d29da01fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.2 MB (431169517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378664f68506dad096d7350b699ea194f61b535f3dd6cdc633a05040b8384918`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:37 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:37 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:00:37 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:00:37 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:15:01 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:15:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:15:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:15:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:15:01 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:15:01 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:15:01 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 21 Jan 2026 19:15:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 21 Jan 2026 19:15:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:15:03 GMT
USER gradle
# Wed, 21 Jan 2026 19:15:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 21 Jan 2026 19:15:04 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e98527feec5a6e3b7d9dd4edae394a807158bda7cdb1fdad45eafe42104a93`  
		Last Modified: Wed, 21 Jan 2026 19:14:36 GMT  
		Size: 155.7 MB (155718940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeda12f1b003a2ca3380a8e8cc2aebad3f80a64963d9279e5cd0a6d08b66eb11`  
		Last Modified: Wed, 21 Jan 2026 19:15:34 GMT  
		Size: 85.5 MB (85516356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53bee24c2030761a9bd96277f055920260bf6f5994d2438f1385fb395768e718`  
		Last Modified: Wed, 21 Jan 2026 19:15:31 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6589948937f9189a250b6c520bb6323641c7803141b04d6f90b9a123a3207f`  
		Last Modified: Wed, 21 Jan 2026 19:15:35 GMT  
		Size: 137.0 MB (136988867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e66a9cef612441ef162f69ac271e59f99b68d03526d7e2039e23f84ae01a365`  
		Last Modified: Wed, 21 Jan 2026 19:15:31 GMT  
		Size: 29.3 KB (29318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:515c752214a81d3876e2cb43b29a3e92dfde526be322ee265b84a333a3b9b8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11344389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8adfbe595923668af4bf3053e2206c6b3950480f3c4dffdbb2491176ed9e7bc`

```dockerfile
```

-	Layers:
	-	`sha256:320f163808ae662cfbf8f173c88f2128076cfaf1ad38fb45bb6eda5fc6b2c3ed`  
		Last Modified: Wed, 21 Jan 2026 21:23:55 GMT  
		Size: 11.3 MB (11322695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a8124cac9f978fc7ae34abb24cd813c3c829ff44b0976153dca92a33ba3f05`  
		Last Modified: Wed, 21 Jan 2026 21:23:56 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
