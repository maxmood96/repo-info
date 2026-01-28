## `gradle:corretto`

```console
$ docker pull gradle@sha256:fa269b0ee1d23cae6144b4b5d4b230ae77e07f6a24a9708e9a6e01b065be6af4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto` - linux; amd64

```console
$ docker pull gradle@sha256:2aae2eec0719a5d5d1f8291497fd795814e5f227cee5d99764305a6213bc791b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.3 MB (466266773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab832543b9cd15b643b837a794da19a477c706301ed811abf8a8f5910492a460`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:10:02 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:10:02 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:10:02 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:10:02 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:10:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 28 Jan 2026 05:33:31 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 05:33:31 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 05:33:31 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 05:33:31 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 05:33:31 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 05:33:31 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 05:33:31 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 28 Jan 2026 05:33:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 28 Jan 2026 05:33:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 05:33:34 GMT
USER gradle
# Wed, 28 Jan 2026 05:33:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 28 Jan 2026 05:33:35 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cb6fcb38396d39f54d43d1b722399b74f95aea87f5b449eac9d4eac383e396`  
		Last Modified: Wed, 28 Jan 2026 04:10:25 GMT  
		Size: 189.2 MB (189191028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2061b4f75402ab630e424c56f730c2d5dd686826b953f25f571edd31a24b688`  
		Last Modified: Wed, 28 Jan 2026 05:34:07 GMT  
		Size: 86.0 MB (86035762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68ba865868bcafa5ac45a93936b4c1e2bdbb8c7685441e61fc5325f5ebb3823`  
		Last Modified: Wed, 28 Jan 2026 05:34:03 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e246aaa01b471c71ecf3af7cf7038a4c58fdb96d9f5511031ffe2b1b586d8d57`  
		Last Modified: Wed, 28 Jan 2026 05:34:08 GMT  
		Size: 137.0 MB (136988868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fddceb8b05cc0f10034155aae1611b7646d2acd700a5c0629e4755535428fd5`  
		Last Modified: Wed, 28 Jan 2026 05:34:03 GMT  
		Size: 25.6 KB (25596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7ef99ec46139dbc4360023e474c785ae046ac9d1be0400a2e676619425a5018c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11360580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb9a759e4c4379fae88ced537d62d0b62413764a069f5fa2098ba032960b328`

```dockerfile
```

-	Layers:
	-	`sha256:849b934c0a1bd14ef5258da9d2cfc4d34d8cc5084fccfab383793e76cdaa17ec`  
		Last Modified: Wed, 28 Jan 2026 05:34:04 GMT  
		Size: 11.3 MB (11338311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952e20d027cd44508fe07db8c7c390bac91570256ef6eaa300b07781a3a12536`  
		Last Modified: Wed, 28 Jan 2026 05:34:03 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:764ec125560b908f9a6ef885243b8b9ba830438b78cbb441ff7d1e759df6280c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.5 MB (462541047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e5a8c49ae2ba705cd9ca85e3c9e38bccaf93c1f8571ad8a3c4c121183de16e`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:31:03 GMT
ARG version=25.0.2.10-1
# Wed, 28 Jan 2026 04:31:03 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:31:03 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:31:03 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:31:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 28 Jan 2026 05:37:44 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 05:37:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 05:37:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 05:37:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 05:37:45 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 05:37:45 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 05:37:45 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 28 Jan 2026 05:37:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 28 Jan 2026 05:37:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 05:37:47 GMT
USER gradle
# Wed, 28 Jan 2026 05:37:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 28 Jan 2026 05:37:48 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a396e73c665f4fa119c9cd20fbfa42ece312688cd9297587073bc7d229c333b4`  
		Last Modified: Wed, 28 Jan 2026 04:31:30 GMT  
		Size: 187.1 MB (187090861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a6fee4ffcdc54d4ec0a8bb85be41f02e3c7c7068aeec17cd7c53688f8d1ab2`  
		Last Modified: Wed, 28 Jan 2026 05:38:20 GMT  
		Size: 85.5 MB (85513681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2319dbb360c1fc9cd41d9fa7b128bb0da366c28f1bc7e4de2165ae7472929322`  
		Last Modified: Wed, 28 Jan 2026 05:38:17 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cca27a5b7d8be8bdc24e009faf3e86619e6dc7f46d1cf2c5f78428e4b3ed98`  
		Last Modified: Wed, 28 Jan 2026 05:38:21 GMT  
		Size: 137.0 MB (136988869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5e5a4581efb51652ac98a701f044960d8c26c0ce6e9b9d1e13125effcfd1e4`  
		Last Modified: Wed, 28 Jan 2026 05:38:17 GMT  
		Size: 29.3 KB (29317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0a1a73bf83ab924fa20bebb86dd135ddb0d90a40c3bdc05bccd7d9078fb3323e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff376bda8fca9a34d4dc18f3acac25a1befe5f95dbf1baf54fac59b9998806e8`

```dockerfile
```

-	Layers:
	-	`sha256:cfe76146e233f078be865f852845923579c838e4b19b42d47ad810a97e538b2b`  
		Last Modified: Wed, 28 Jan 2026 05:38:17 GMT  
		Size: 11.3 MB (11337348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a1e6c20e4e409903563ac41b5406f60281f7101b3c76d63ebdbf1cc9d8fe780`  
		Last Modified: Wed, 28 Jan 2026 05:38:16 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
