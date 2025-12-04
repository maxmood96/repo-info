## `gradle:8-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:d4551ba7e88ee5241bf27beef03f735aa5e0ceab7a903e588cb70872657784d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:abdcd688aabbb5e7d88ad3df99f405081ccbc403709e450a3786997460f38144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.8 MB (430758199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c53ba56a2f8da0c055ef8c60722e57ea89b237471d9357ebf970d88bc88f163`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:00 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:23:00 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:23:00 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 03 Dec 2025 21:12:50 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:12:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:12:50 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:12:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:12:51 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:12:51 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:12:51 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 03 Dec 2025 21:12:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 03 Dec 2025 21:12:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:12:53 GMT
USER gradle
# Wed, 03 Dec 2025 21:12:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 03 Dec 2025 21:12:54 GMT
USER root
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776c9643cd4150afa1afb3b1c3571d4b01d14b3d59564d8995c086d0ec8c9eb7`  
		Last Modified: Wed, 03 Dec 2025 21:11:23 GMT  
		Size: 153.3 MB (153313008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c4d0e24148452ec2c653f8d81bdf0a208b76926ae088753f2d353b2dc7a563`  
		Last Modified: Wed, 03 Dec 2025 21:13:41 GMT  
		Size: 86.0 MB (86024372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c615edbc411261d4bec1edfaee760cb49cb57c1c7b9582806938f04f6b2830`  
		Last Modified: Wed, 03 Dec 2025 21:13:29 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e50b9b66aa30680adab555cd332e439c7721616a4b0fd5026b85d90b6c364aa`  
		Last Modified: Wed, 03 Dec 2025 21:13:25 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00b526bcd49824873be3b0cd74e266241de2bdcdc0163d15c9e494125da0337`  
		Last Modified: Wed, 03 Dec 2025 21:13:29 GMT  
		Size: 54.9 KB (54921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:83716251d1dbe2621fac2c57a42fc1bcb0275180f8668b30934bbafc3a3edf4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f821787c6dfaa3a67c845c3a383800a11a1456993f0a03f304dc2b544ba6fbc5`

```dockerfile
```

-	Layers:
	-	`sha256:9b62f854891cb62ebb30be8e56dc59821b00d8a3e0802fc2abc12fef4b27b682`  
		Last Modified: Thu, 04 Dec 2025 00:20:37 GMT  
		Size: 11.4 MB (11365984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:383b45ccc52309d3a62529ba3fea00fdad15457bc6a6e2e668135c3c16b6dd70`  
		Last Modified: Thu, 04 Dec 2025 00:20:38 GMT  
		Size: 21.5 KB (21520 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:09bdbc69e91b999dd3e42745c7083d98bdf932af8c08ccdbe46b994d76fe8fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.7 MB (427711487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a581b2e778793d4e01f56ccb7256fa49a5eaf4253bd84e6ef02b4acc3e02e87`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:28:24 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:28:24 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:28:24 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:28:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 03 Dec 2025 21:12:13 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:12:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:12:13 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:12:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:12:14 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:12:14 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:12:14 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 03 Dec 2025 21:12:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 03 Dec 2025 21:12:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:12:16 GMT
USER gradle
# Wed, 03 Dec 2025 21:12:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 03 Dec 2025 21:12:17 GMT
USER root
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8861eb4f7a0b53ecbb0f75902386ed6e16a790f86d286d0c6485f438864cf0c`  
		Last Modified: Wed, 03 Dec 2025 21:11:49 GMT  
		Size: 151.9 MB (151860266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dc5ef0acf4a7f63ee1e05a79eb1ac91d71a2cb2e0d44dabdb38a32d544e3d3`  
		Last Modified: Wed, 03 Dec 2025 21:13:11 GMT  
		Size: 85.5 MB (85525396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994ea033e201a7fe33a4601eec33785fec61c68ce3280dedf5cfa618c393334a`  
		Last Modified: Wed, 03 Dec 2025 21:12:57 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa706045dde19fc86cc96cb76aa05c883c7fe616e7dff18f7921d56c98833bdc`  
		Last Modified: Wed, 03 Dec 2025 21:12:50 GMT  
		Size: 137.4 MB (137395197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474147eeb8f4fca57d922e4b6cf4a8a46e3db049a1b52dc43d399eab906319a3`  
		Last Modified: Wed, 03 Dec 2025 21:12:57 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:c0c4de355a1817ae8c6639a0fda4b2fe9082780f2a44c5c9c4d3f54c3584b633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2de10737d7954c24de3e4904d18f6ad707e8ffd5418a68e4616d78d4be8d0ab`

```dockerfile
```

-	Layers:
	-	`sha256:e9bb5b93d3c29697040945a1cc781d2590958575e466eb56ce3612bf9f559f16`  
		Last Modified: Thu, 04 Dec 2025 00:20:46 GMT  
		Size: 11.4 MB (11365827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fbfebeab4205ba1b99565b76b21fc269741384e9f11a2a73cfa469bbdb4c309`  
		Last Modified: Thu, 04 Dec 2025 00:20:48 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
