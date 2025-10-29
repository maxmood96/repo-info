## `gradle:9-jdk25-corretto-al2023`

```console
$ docker pull gradle@sha256:87c3709893da841627b71a624190c662ae54fd013c823000a5cf238c577cd983
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a7fc25af359effabfcfa38fb91a275e0fe17c21e331a664664dc88b1105f61d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.3 MB (464313433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ed035c094fd0e0234bb8c1225246faafce3591a40c61015a028b38a3cca82e0`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:56 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:56 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8-1
# Tue, 21 Oct 2025 20:48:19 GMT
ARG package_version=1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 29 Oct 2025 17:33:30 GMT
CMD ["gradle"]
# Wed, 29 Oct 2025 17:33:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 29 Oct 2025 17:33:30 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 29 Oct 2025 17:33:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 29 Oct 2025 17:33:30 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 29 Oct 2025 17:33:30 GMT
WORKDIR /home/gradle
# Wed, 29 Oct 2025 17:33:30 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 29 Oct 2025 17:33:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 29 Oct 2025 17:33:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 29 Oct 2025 17:33:32 GMT
USER gradle
# Wed, 29 Oct 2025 17:33:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 29 Oct 2025 17:33:33 GMT
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
	-	`sha256:344910cae35184dc555ba370ed61ae5db23bfab48d5c79c7d0b670a5e5215e0c`  
		Last Modified: Wed, 29 Oct 2025 17:34:29 GMT  
		Size: 85.6 MB (85559517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081065e3feb89f4333e4cbe6542194951256b7d5ea94c8e8775bc02ce8c08711`  
		Last Modified: Wed, 29 Oct 2025 17:34:20 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c295be73b6407e4125dbea2ce4182c9645220f4c80daec1070f4bcd770555`  
		Last Modified: Wed, 29 Oct 2025 17:34:11 GMT  
		Size: 135.5 MB (135521660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59ca9da8ffea62425a3f37e63969bc72e03db338c75d17dde5c1fd7a0cd1717`  
		Last Modified: Wed, 29 Oct 2025 17:34:19 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:60e41fa800ba0f5596b7552ea527daedf71a9ffaafcc16ed68a56e3f8d98d5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11343210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df81d90f82e260b7bd302790f1423e328bfe58f160ae4a7fd2ec00e4ddeadcc`

```dockerfile
```

-	Layers:
	-	`sha256:e67d30ba7ba046e035c24fef79a29c46bfb234ec8ba4d6f4c0d807b09dbce847`  
		Last Modified: Wed, 29 Oct 2025 20:24:50 GMT  
		Size: 11.3 MB (11320990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e430e9eb7d6cdd57f9fffaea44ca139c9521ddacd43357fc297fd50551a10396`  
		Last Modified: Wed, 29 Oct 2025 20:24:50 GMT  
		Size: 22.2 KB (22220 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e0545e6a7ca2ac585b8e29ece3e80ecccc54800bed8f1f86e2f18795c935ef3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.7 MB (460657975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd067f117ca4e43a9900a3d599ed4bd84864e0d3c476236d9f673446e6026a9`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:59 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8-1
# Tue, 21 Oct 2025 20:48:19 GMT
ARG package_version=1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 29 Oct 2025 17:33:23 GMT
CMD ["gradle"]
# Wed, 29 Oct 2025 17:33:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 29 Oct 2025 17:33:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 29 Oct 2025 17:33:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 29 Oct 2025 17:33:23 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 29 Oct 2025 17:33:23 GMT
WORKDIR /home/gradle
# Wed, 29 Oct 2025 17:33:23 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 29 Oct 2025 17:33:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 29 Oct 2025 17:33:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 29 Oct 2025 17:33:26 GMT
USER gradle
# Wed, 29 Oct 2025 17:33:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 29 Oct 2025 17:33:26 GMT
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
	-	`sha256:cbfd90519e72434574e1f1d733ebc89a329c7998249c0e98a9dc5e4118a946f3`  
		Last Modified: Wed, 29 Oct 2025 17:34:28 GMT  
		Size: 85.1 MB (85087585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac3c5f0de06c94b0d9b0ef4ee8196793491f9ded75e77ad156b995e69a57970`  
		Last Modified: Wed, 29 Oct 2025 17:34:20 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1525af82ceaa9fdfe7ceabe4a226cdc20155917a9aed3d26c178bc3a2c23802`  
		Last Modified: Wed, 29 Oct 2025 20:35:58 GMT  
		Size: 135.5 MB (135521663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea495578e631527ab368fae6214db30aca28257ac35ae47f8cca2b96d642015`  
		Last Modified: Wed, 29 Oct 2025 17:34:20 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:263a5bdaa9b2a7b132b1ea08789851f37fcf58c1565dcd0b8fe8a1aa6c42e1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11342467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a598438556429818b40e5499053c5525ee90de84100a70fd7d39c543ffb03541`

```dockerfile
```

-	Layers:
	-	`sha256:97da51f702832faf4b66a6bcdeefa0969e8b92fef0607ed145bbc9ecfd5c38bc`  
		Last Modified: Wed, 29 Oct 2025 20:24:59 GMT  
		Size: 11.3 MB (11320027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:034dcde399f7bbce97797481a04022e21bd377f286dd24142ba3b9a49337cced`  
		Last Modified: Wed, 29 Oct 2025 20:25:00 GMT  
		Size: 22.4 KB (22440 bytes)  
		MIME: application/vnd.in-toto+json
