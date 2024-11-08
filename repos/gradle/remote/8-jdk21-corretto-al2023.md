## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:939bdd2c770b1872b24ffb69c75eee6a4c3ccf6c8eb299a7558e543e212d1df1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:5a50d094cef300160a843d459f32a3213e4a1571a36262a3fe106b2b2ef20618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.5 MB (429469890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e637e651652a6e32934bee367aa218da4874e8985eb12c9a690c19e4e2459e26`
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
# Wed, 06 Nov 2024 04:13:47 GMT
CMD ["gradle"]
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Nov 2024 04:13:47 GMT
WORKDIR /home/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 06 Nov 2024 04:13:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER gradle
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8359f338e081ca7a1c86734851b92cd4a5edb2e0ff59e71e19a0f2a7671796`  
		Last Modified: Mon, 21 Oct 2024 18:57:15 GMT  
		Size: 169.7 MB (169703760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8431386fed63bdf360ca8501fa024e3eae770f816c8175f2d331c541e400abac`  
		Last Modified: Wed, 06 Nov 2024 20:17:47 GMT  
		Size: 70.6 MB (70635974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c895bc15ff2766d0907a9cb875ccda4b35b570bd71ed54585a989fd633451be5`  
		Last Modified: Wed, 06 Nov 2024 20:17:45 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f03737f101e17e803ec9bdbe68603bff847dcadb346e850257070fc7efe066d`  
		Last Modified: Wed, 06 Nov 2024 20:17:48 GMT  
		Size: 136.7 MB (136729732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d922da230cd9c66266f8334e4d1c171accb28360b874f250051ac4dab63f623`  
		Last Modified: Wed, 06 Nov 2024 20:17:46 GMT  
		Size: 54.9 KB (54914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:3ac56fa14b409fb1c6a85215759e0050473e495dc8cf124a4fb333027d5a349b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10754286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc419fb438519cd96772e18b88c99c649a0912470581ed524d2335e8c955c44`

```dockerfile
```

-	Layers:
	-	`sha256:402c49287be544055d8b0d31ce13b3343c9999b01b6287133316c94a5a2919f1`  
		Last Modified: Wed, 06 Nov 2024 20:17:46 GMT  
		Size: 10.7 MB (10733759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a2d6a548b1f22791261aa6e934d851643143913e4d9fb910f94d9ae67d5fcb3`  
		Last Modified: Wed, 06 Nov 2024 20:17:45 GMT  
		Size: 20.5 KB (20527 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7042c627ceed55879944c3fbf701be0e58cbea0bb777a4995ea3b721395a638a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.5 MB (426499812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbd78aed5515ef49ade772f7a54dee7b96d8101b7a8fd6b60a0c0e4128fad24`
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
# Wed, 06 Nov 2024 04:13:47 GMT
CMD ["gradle"]
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Nov 2024 04:13:47 GMT
WORKDIR /home/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 06 Nov 2024 04:13:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER gradle
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:ec188ec9ab67d19829a9f75d24a165b6b31e1c611a03fdfabfdf4f1950a2c30a`  
		Last Modified: Wed, 06 Nov 2024 22:31:41 GMT  
		Size: 51.4 MB (51424001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdb671156c1aad95b344295e84d111495c317a27e4855ebbdd44d807f852c98`  
		Last Modified: Thu, 07 Nov 2024 22:04:23 GMT  
		Size: 167.9 MB (167931592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fc332016cb5da086280fe96b3f66989eef8f10040307228efc041797365d6b`  
		Last Modified: Thu, 07 Nov 2024 22:51:46 GMT  
		Size: 70.4 MB (70353280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b992b082ac8311616352d39ae0b24501c79bb9d2fc11771288c596f1f199bb7`  
		Last Modified: Thu, 07 Nov 2024 22:51:44 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f65adeb875113e94ba11ce1a2e01cb2e185c199ab17133380d2af8decf18ad8`  
		Last Modified: Thu, 07 Nov 2024 22:51:48 GMT  
		Size: 136.7 MB (136729733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4416e0afc3018a1c2dfffa34b48ba5718b730897e2472e5babca377c4b3be0e`  
		Last Modified: Thu, 07 Nov 2024 22:51:44 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:89d3a5b8e9f1d745e006eaa5cea2e27b13f60cccd589ee64521c6c04c5f99a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10753508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e4c2625bd6745363e41496ee7c0ab51ac627eca16ac4923f440da2d40f2366`

```dockerfile
```

-	Layers:
	-	`sha256:9a7c35d60b548e8033ca2b3b5efb9d9fdea8ad705b298b66753de9a9713ffde2`  
		Last Modified: Thu, 07 Nov 2024 22:51:45 GMT  
		Size: 10.7 MB (10732761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:689abe57103d59b540b6b51679cd86ddf806bb9f1be11ff4b1a37d572c0cb2cd`  
		Last Modified: Thu, 07 Nov 2024 22:51:44 GMT  
		Size: 20.7 KB (20747 bytes)  
		MIME: application/vnd.in-toto+json
