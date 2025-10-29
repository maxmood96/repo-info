## `gradle:jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:684c97c874945bc9edcc4565efd1249fe9908974d695bc6e4f47dfdbf4b6e079
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:28e0cc7c0f8c9db34e5d59dff59deac9641521767b30ca85aedbb598e7048cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432074884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf94459164f5ad5c21be671a048037602ec81651aac90d00b9f402458e71b96`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:56 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:56 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
ARG package_version=1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 29 Oct 2025 17:34:41 GMT
CMD ["gradle"]
# Wed, 29 Oct 2025 17:34:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 29 Oct 2025 17:34:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 29 Oct 2025 17:34:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 29 Oct 2025 17:34:41 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 29 Oct 2025 17:34:41 GMT
WORKDIR /home/gradle
# Wed, 29 Oct 2025 17:34:41 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 29 Oct 2025 17:34:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 29 Oct 2025 17:34:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 29 Oct 2025 17:34:43 GMT
USER gradle
# Wed, 29 Oct 2025 17:34:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 29 Oct 2025 17:34:44 GMT
USER root
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c18700ed5b667d3e3ad2c64896284eb1ca36287f16a71ecfb7d35d0da454038`  
		Last Modified: Wed, 22 Oct 2025 00:50:39 GMT  
		Size: 156.9 MB (156935240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4cf5385270d394184374b421c9a1cbc197851c8b6a1d2d5446c5057eff79a3`  
		Last Modified: Wed, 29 Oct 2025 17:35:31 GMT  
		Size: 85.6 MB (85556220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbce058fd2491fcf873e29d36f7022794b19c280d010e695b9dc77618e922af`  
		Last Modified: Wed, 29 Oct 2025 17:35:23 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0e80bef49f203f9cc1462e1a983b324239f97d93816e60eccb5c123cbe8ada`  
		Last Modified: Wed, 29 Oct 2025 20:43:39 GMT  
		Size: 135.5 MB (135521720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74526dea67979f111c781f9dd605e66da41123fe5ed754dfce0e2a18cb92c7f6`  
		Last Modified: Wed, 29 Oct 2025 17:35:24 GMT  
		Size: 54.9 KB (54894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b111c7ca56ca9cc1d2c22528f65a5f4a5af8ea50078cf9dff4229cfc92aece22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11327843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e73e745ca969b72f6f4b7158dce9e4fcb92889f0fcd3893384fcb82484da40`

```dockerfile
```

-	Layers:
	-	`sha256:8756a4c6e605f6103c6f3fad48d5f190dc0886923f8bee63bad90ef757a3f9fa`  
		Last Modified: Wed, 29 Oct 2025 20:22:51 GMT  
		Size: 11.3 MB (11306395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:754d4b741bd2577631c85ded66a5fd9b5661fb011c7128b0816923f2cbd4eb08`  
		Last Modified: Wed, 29 Oct 2025 20:22:52 GMT  
		Size: 21.4 KB (21448 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e88a61b5256361f340d0d6966f422cb20328999cdf5a809dd35fcd0b751f73f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.3 MB (429305894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d329fc2987df04ad1f28ac44c1eb63d51e721d8d01e4a194d651b051ec5339f`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:59 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
ARG package_version=1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 29 Oct 2025 17:34:32 GMT
CMD ["gradle"]
# Wed, 29 Oct 2025 17:34:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 29 Oct 2025 17:34:32 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 29 Oct 2025 17:34:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 29 Oct 2025 17:34:33 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 29 Oct 2025 17:34:33 GMT
WORKDIR /home/gradle
# Wed, 29 Oct 2025 17:34:33 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 29 Oct 2025 17:34:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 29 Oct 2025 17:34:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 29 Oct 2025 17:34:35 GMT
USER gradle
# Wed, 29 Oct 2025 17:34:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 29 Oct 2025 17:34:36 GMT
USER root
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6803c97e6c0d717ec8eb0dfce3611037cd37d1539766448f9235c54a09a795`  
		Last Modified: Tue, 21 Oct 2025 22:11:31 GMT  
		Size: 155.7 MB (155747849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eab0442746f6d163f1dc7b88f3f5c0e93046cd223e16a9da020752982238fb7`  
		Last Modified: Wed, 29 Oct 2025 17:35:31 GMT  
		Size: 85.1 MB (85083975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fde8e97b586586563b331b0eed30cb9c2a5d8972488ca1dd11ea988ac5477c1`  
		Last Modified: Wed, 29 Oct 2025 17:35:18 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87a4c8f46bfc9dca376b3f8506c473661da4efead8a07c28e9e0fcac0547a46`  
		Last Modified: Wed, 29 Oct 2025 17:35:09 GMT  
		Size: 135.5 MB (135521658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953a1bcd5dda9bbd499cc1fcd41a5a7e536779210ad0d21e54aceafb54058751`  
		Last Modified: Wed, 29 Oct 2025 17:35:18 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:3a531b25192f384760a01ede7674b4290f5578717198b952dabe20213dac698c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11327039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873e3bb626f51bdd54721fe3f9a41e9cf846a2a59823349d6070866ff8e4694e`

```dockerfile
```

-	Layers:
	-	`sha256:8df6c72f08eea2b0295d908d8a116f37b4ab8b73c8ab3142d2328ed5c1dbc4b8`  
		Last Modified: Wed, 29 Oct 2025 20:23:01 GMT  
		Size: 11.3 MB (11305394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7557b8cb9c451ae20639348b89d6c67dac50ec0a559c3e3be73fbc4de663c43`  
		Last Modified: Wed, 29 Oct 2025 20:23:02 GMT  
		Size: 21.6 KB (21645 bytes)  
		MIME: application/vnd.in-toto+json
