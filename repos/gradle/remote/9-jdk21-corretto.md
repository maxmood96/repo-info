## `gradle:9-jdk21-corretto`

```console
$ docker pull gradle@sha256:54c0e68ef126906359ea5440d4d3f9edd03818c50b4650655b379e03de7ef633
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:9cb28955cadf1108a171d104645c00a063c85757d6e2530bc52c1bdf52734a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.4 MB (445409568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55680a149b7c8527552006b6b8d6dd474251a2aed49614cc79b104a1d7fc5a56`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:06:16 GMT
ARG version=21.0.9.11-1
# Wed, 05 Nov 2025 01:06:16 GMT
ARG package_version=1
# Wed, 05 Nov 2025 01:06:16 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 05 Nov 2025 01:06:16 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 05 Nov 2025 04:50:28 GMT
CMD ["gradle"]
# Wed, 05 Nov 2025 04:50:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 05 Nov 2025 04:50:28 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 05 Nov 2025 04:50:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 05 Nov 2025 04:50:28 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 05 Nov 2025 04:50:28 GMT
WORKDIR /home/gradle
# Wed, 05 Nov 2025 04:50:28 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 05 Nov 2025 04:50:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 05 Nov 2025 04:50:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 05 Nov 2025 04:50:31 GMT
USER gradle
# Wed, 05 Nov 2025 04:50:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 05 Nov 2025 04:50:31 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d298c96cc089701668f1f26ebc2ed62153aa52cd816ed6691a3e4aa37f8b318`  
		Last Modified: Wed, 05 Nov 2025 02:50:01 GMT  
		Size: 170.2 MB (170217752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dec9a7d121d993e74c7c75ec515470fdcb46e749ada6b2d0e373487e7ecf7f0`  
		Last Modified: Wed, 05 Nov 2025 04:51:24 GMT  
		Size: 85.6 MB (85612342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7c8838f3694f04837b7186addd6cec45ce2b69f9e473f1223c9cd98f960782`  
		Last Modified: Wed, 05 Nov 2025 04:51:11 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a89218902a7b0a924ca0f2f1a09e229993009d1703612b28f7b33987c09e1`  
		Last Modified: Wed, 05 Nov 2025 06:33:40 GMT  
		Size: 135.5 MB (135521661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc4cc3ec06274cf705cfce87a7fad984eed7eb624ad1386713aaa8d7460985f`  
		Last Modified: Wed, 05 Nov 2025 04:51:11 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:113fb8eaaa27641d9032b8e6a128b9287ca58aa6321be2b304d5aa3473be3bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11337374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d499a0589e18b06235a58966b782dcbb26a82c1ce4e44fd36133f88b4b9013`

```dockerfile
```

-	Layers:
	-	`sha256:4688b2437c7cf8c8ed4b23d9caf7887df46c8f512b7275fc45b9fded93b7079a`  
		Last Modified: Wed, 05 Nov 2025 06:21:16 GMT  
		Size: 11.3 MB (11315772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62c2bbad74cda26f51c18daa8d15884048b80c5e01d1ab8f56ec3353d775c0b`  
		Last Modified: Wed, 05 Nov 2025 06:21:16 GMT  
		Size: 21.6 KB (21602 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ff8f8bb6a29e302394c98b4d08cab6d0b736621d0d9676ebd55de0d1524f3e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.1 MB (442127595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55fffb63b41a0a7538974f9b8bd22c216743a4a5969dc546a5dd912194953389`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:23 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 22:14:23 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:14:23 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:14:23 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 06 Nov 2025 23:11:52 GMT
CMD ["gradle"]
# Thu, 06 Nov 2025 23:11:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Nov 2025 23:11:52 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Nov 2025 23:11:52 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Nov 2025 23:11:52 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Nov 2025 23:11:52 GMT
WORKDIR /home/gradle
# Thu, 06 Nov 2025 23:11:52 GMT
ENV GRADLE_VERSION=9.2.0
# Thu, 06 Nov 2025 23:11:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Thu, 06 Nov 2025 23:11:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Nov 2025 23:11:55 GMT
USER gradle
# Thu, 06 Nov 2025 23:11:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Nov 2025 23:11:56 GMT
USER root
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc78c02c91f4f2038e786f731208f8cc3446308a4d3f914fe9891f94f2eb9e`  
		Last Modified: Thu, 06 Nov 2025 23:11:22 GMT  
		Size: 168.5 MB (168474554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0124d90ba93ce7b6e4aede9f055adc7923311a5764425d0bd98679cd3db8c269`  
		Last Modified: Thu, 06 Nov 2025 23:12:53 GMT  
		Size: 85.2 MB (85168415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86d8862dd73a7a7fae358608c560c6c5d4a7faa7dbb76f6be5b6cc6fa9df6e2`  
		Last Modified: Thu, 06 Nov 2025 23:12:34 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3f37bd54faf45623e59fd41c39d70e3ce82cd6c8bfa39320dd8a4087c1a384`  
		Last Modified: Thu, 06 Nov 2025 23:12:29 GMT  
		Size: 135.5 MB (135521729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad874b759c279823c05389be47fdb8872c8ddde0fde24e06038c88b0bee3374e`  
		Last Modified: Thu, 06 Nov 2025 23:12:35 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:37f136708a861a12867d9525640a00ea3570bc29aeaa49974d8f1ad1671a4713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11336573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c80a50f0db12de9b5817229c55fe335c8cb32e5e191ecf6ec2a8dc1de92f224`

```dockerfile
```

-	Layers:
	-	`sha256:2c36a9439c223a055697d32e5739f5fbad93ad3f0c888166828bedc4f2644d3f`  
		Last Modified: Fri, 07 Nov 2025 00:23:20 GMT  
		Size: 11.3 MB (11314774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3aa4ba6f9c1316bc4ef12edb42cd2107ebbb53a1fa97b699c5ff86bd3ae1ee28`  
		Last Modified: Fri, 07 Nov 2025 00:23:21 GMT  
		Size: 21.8 KB (21799 bytes)  
		MIME: application/vnd.in-toto+json
