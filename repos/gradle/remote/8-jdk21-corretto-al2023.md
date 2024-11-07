## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:59906ff9f34c9bd1dcde657e8216651d5959d762fe07f645049f0196d45d30d5
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
$ docker pull gradle@sha256:e9c03302aaae295c2704ca31544eeff15f36beed077431c376e52a3f9dee1421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.5 MB (426490107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023b133b2e61032c2fe4dd783fc56a18c5da3cb0c59296a1dc32480599a1494a`
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
	-	`sha256:923a2071aa1c62af0f57aa46e86e64587ba93da0a38eaf52d228227154730e17`  
		Last Modified: Tue, 15 Oct 2024 02:53:59 GMT  
		Size: 51.4 MB (51424527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccbc2100cda5cd86ae636d0e242db173ccdd510ca9963e42485bf28543b809d`  
		Last Modified: Mon, 21 Oct 2024 21:04:04 GMT  
		Size: 167.9 MB (167930883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b807c348ee899eda53b2b6473581c6fb793e9f776550d03ed63c98447b642e6c`  
		Last Modified: Wed, 06 Nov 2024 20:12:57 GMT  
		Size: 70.3 MB (70343744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb610c04b2cf0baeb44569b270b54f821fdaafbb85cd8ad2acbb588a4f60ef8`  
		Last Modified: Wed, 06 Nov 2024 20:12:54 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31d7877d063fac24802d5b49b496a82665f0102fec6eea9a0851e54222195b8`  
		Last Modified: Wed, 06 Nov 2024 20:12:58 GMT  
		Size: 136.7 MB (136729735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a03e2e547e07ada16d36b3a31c931584377e95874ca888ff254836f5330a89`  
		Last Modified: Wed, 06 Nov 2024 20:12:55 GMT  
		Size: 59.5 KB (59539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:861be1664049c6662a2a438566f4f66cb7e89284fc647ee03c74922b474f5f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10753531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bce5575df9a46ad44562b6475d78bb55b98445bcc537b4cf4a56c264092ca43`

```dockerfile
```

-	Layers:
	-	`sha256:2584d153141231f0edc62f7d86a2c989a04707f41d881fc12bccf01bc105e2f7`  
		Last Modified: Wed, 06 Nov 2024 20:12:55 GMT  
		Size: 10.7 MB (10732783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfce390cd3e754297c3aa705733b11bffd0fcbd77a54fe0a41cb98cc76367cdf`  
		Last Modified: Wed, 06 Nov 2024 20:12:54 GMT  
		Size: 20.7 KB (20748 bytes)  
		MIME: application/vnd.in-toto+json
