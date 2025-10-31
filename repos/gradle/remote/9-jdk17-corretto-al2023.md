## `gradle:9-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:aa559214ecd4bbd3802c7a05702f985e1647cc0ab1fbf7dab59004e0ec7ee01e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:f80e04fc8f4abad75ab55cb51e0386b833775efbbc696d2c1d25439a7f74b01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432123895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206a5a4c43b6de2bbf769c5f973153dfc224f4f541f0b270aeecc8e55081465f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:05 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:05 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:05 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:05 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 31 Oct 2025 01:11:28 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:11:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:11:28 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:11:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:11:29 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:11:29 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:11:29 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 31 Oct 2025 01:11:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 31 Oct 2025 01:11:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:11:31 GMT
USER gradle
# Fri, 31 Oct 2025 01:11:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:11:31 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc93996f720aafe561378567487aad4cac58bd5c93215d7c30b4dc3cb269fe7d`  
		Last Modified: Fri, 31 Oct 2025 01:11:05 GMT  
		Size: 156.9 MB (156930995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112012f5d977837d6949520db8bd8f0c461731015d5f74f9afd25e68fa05b59f`  
		Last Modified: Fri, 31 Oct 2025 01:12:19 GMT  
		Size: 85.6 MB (85613360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b791c9c0fa14e8f5502cfeabdcedc281997e9f929359b6ca1b347b1201af1b7f`  
		Last Modified: Fri, 31 Oct 2025 01:12:09 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6831ac63d24bd93ba7dc441df0cd1b260e4f08c5f56dbb8fb25cc6a95c284a08`  
		Last Modified: Fri, 31 Oct 2025 02:27:43 GMT  
		Size: 135.5 MB (135521732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcd66fb43a9e581e47c4eb50111a283f1b1f7c59e29f57142453d68e12af4ae`  
		Last Modified: Fri, 31 Oct 2025 01:12:09 GMT  
		Size: 54.9 KB (54893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:138b43f73b23d12e05f039177fafd4492a1fbf7c8409f05ba8c2944553447bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11334805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aad758ef11aa737bbab678887765cc836867e183d0abbad66a277068694e78`

```dockerfile
```

-	Layers:
	-	`sha256:57ec62ff13cdbb3087112d5c1f120c107a57ee25cfe4c5b45e67b3e4253f2faf`  
		Last Modified: Fri, 31 Oct 2025 02:23:17 GMT  
		Size: 11.3 MB (11313358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9c2cbcbff0019ab88879ffe0c8b8d771e944c860bc4e09481d9b071ffd65ceb`  
		Last Modified: Fri, 31 Oct 2025 02:23:18 GMT  
		Size: 21.4 KB (21447 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5410dfff2f632aef457c91a00e1c174f57653d2216520bd2106b1c7c1384ad11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.4 MB (429393755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:961ebfe75d8c03d7501cc1339124ad7d864dd011f121bcd10bbc1c22e99fc40d`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:31 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:31 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:31 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:31 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 31 Oct 2025 01:12:02 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:12:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:12:02 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:12:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:12:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:12:03 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:12:03 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 31 Oct 2025 01:12:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 31 Oct 2025 01:12:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:12:05 GMT
USER gradle
# Fri, 31 Oct 2025 01:12:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:12:06 GMT
USER root
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e64fbe357a20bde5fc5f6090c96fc58b45b69ba5f931228fff57e15660663b`  
		Last Modified: Fri, 31 Oct 2025 01:11:37 GMT  
		Size: 155.7 MB (155741138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b994b708cb03d5def2252f2dd4cb3d8e143916f0a2739bcf325d277a4dd6b1d`  
		Last Modified: Fri, 31 Oct 2025 01:12:51 GMT  
		Size: 85.2 MB (85167831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcafa20e0336c0ba6c132ba230cffe3151cb38f757752018f48723d16e34562`  
		Last Modified: Fri, 31 Oct 2025 01:12:44 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ecc9ada9efccab1ac094e7fc5e8ef313f0de5b247b01ce90ac39a3063ff5a4`  
		Last Modified: Fri, 31 Oct 2025 01:12:39 GMT  
		Size: 135.5 MB (135521732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6c5dc4353a0c951a76a4957a1473e3910ebee167d7c397babd9e8ff0a3882d`  
		Last Modified: Fri, 31 Oct 2025 01:12:44 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:60c7c2e7a8956bfc2b6266c6f6e4fccc66be7bade6f15517fada8eb1c9067ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11334002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bc39c1ddf2ac3074f66a0c70576fc3e8f2b1a8dd63731181b7decbc6e7ff47`

```dockerfile
```

-	Layers:
	-	`sha256:b24222fa63f81c97e93d7a660b6b3b5298e9ada50cf3e740f5c54d2dad1c7a91`  
		Last Modified: Fri, 31 Oct 2025 02:23:27 GMT  
		Size: 11.3 MB (11312357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37adf1c45f03b30ed9f798870df2ff2b94d5408ffb4affd2d2a294816c2cd10c`  
		Last Modified: Fri, 31 Oct 2025 02:23:27 GMT  
		Size: 21.6 KB (21645 bytes)  
		MIME: application/vnd.in-toto+json
