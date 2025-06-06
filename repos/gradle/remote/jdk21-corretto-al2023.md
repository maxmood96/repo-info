## `gradle:jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:33ddff495458d2c591ce81a346e064fe447c51a634729d3a94579e8e1e4e5a0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:bcfbc6a241c627d3ee2d8b6af710b21207b8da2d955d6ebc010bf0f76e028e71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.6 MB (444558883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9620646cba68ad8186ab5560fba5876819b954d73453c402dc426fab51a365b2`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Thu, 15 May 2025 19:36:56 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1dd26f3fd48ad2bdc7fb164ac55c6714a2039d97013de0c5f2b15de0d74ec1`  
		Last Modified: Mon, 19 May 2025 23:45:51 GMT  
		Size: 169.8 MB (169833486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92de9bf20cee6fa28e3ba784b58bbdcdbd3287476ff4b1c0917625a7aef389b2`  
		Last Modified: Thu, 05 Jun 2025 20:21:31 GMT  
		Size: 83.7 MB (83658607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb0f8f456b390a6c57135a60c36afc884d3e1b4a2f6dcfb364c593905c84ab4`  
		Last Modified: Thu, 05 Jun 2025 20:21:24 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd690f9b7c3974d7223ea7560c3ae795f216b3d9ebbd0e74dff865b220f561b7`  
		Last Modified: Thu, 05 Jun 2025 20:21:33 GMT  
		Size: 137.4 MB (137395505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a678be3e39cf086cb67b51edfb2fca41456f925274b147d7639853a184235e`  
		Last Modified: Thu, 05 Jun 2025 20:21:24 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:d2e7d151538ce30bb76dd1622cd008cc6cd1f153fbbe68d6be068d518bc186d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11293861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6f6dc523afdd68402b946e30e2317fe20596b4abea18d7c9ec300644501ab83`

```dockerfile
```

-	Layers:
	-	`sha256:a0cfcf5d5dfed2c3ba64923de21b22259def8be8ab48e8452924b9729bf185cc`  
		Last Modified: Thu, 05 Jun 2025 20:21:18 GMT  
		Size: 11.3 MB (11271662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fe97c4a862e32240bd9318bd5f11cca8d5767be8068a9c34d2bb16c66612505`  
		Last Modified: Thu, 05 Jun 2025 20:21:19 GMT  
		Size: 22.2 KB (22199 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:942a3d063e708ff55153e6b69059ca048e44528fa8c30308054ed5f117fcbd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 MB (441396137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42e0e86615b756c35a401f1c17ccc08cbc926993d040b87dcecb85c4aeb8d0d`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 05 Jun 2025 16:04:16 GMT
CMD ["gradle"]
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 05 Jun 2025 16:04:16 GMT
WORKDIR /home/gradle
# Thu, 05 Jun 2025 16:04:16 GMT
ENV GRADLE_VERSION=8.14.2
# Thu, 05 Jun 2025 16:04:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER gradle
# Thu, 05 Jun 2025 16:04:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7197a12f450794931532469d4ff21a59ea2c1cd59a3ec3f89c035c3c420a6999
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 05 Jun 2025 16:04:16 GMT
USER root
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd140d5ff7cfeed9c5da7c3591b30e13df8be78b63c8efafddcaf1920a14be7`  
		Last Modified: Tue, 20 May 2025 00:51:53 GMT  
		Size: 168.1 MB (168137719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e7db4d4aa931d484763a5d0f2bedc960441d79bd875ca2228f8259285bfcac`  
		Last Modified: Tue, 03 Jun 2025 14:57:05 GMT  
		Size: 83.2 MB (83235952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a13af800c769fd6ad9dcf1a4f36391248c96f43c533ed93caa74cb4a56e4c9`  
		Last Modified: Tue, 03 Jun 2025 14:56:55 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d3eeed8304554a40cad545d7bed904726279c232d6ac9182cfae99955bcd73`  
		Last Modified: Fri, 06 Jun 2025 02:30:43 GMT  
		Size: 137.4 MB (137395507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b506a4f1f171e71e9e1624583315e8f5f240f6dfcbb567c743e7555f651d33`  
		Last Modified: Fri, 06 Jun 2025 02:30:33 GMT  
		Size: 59.5 KB (59543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:d36fdb3004a100adbd2ecb0034773f1af66001e67f1587c0eb8a9470ff75402e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11293109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea43a559c0ff365c6330ddc9fbe6d059d54c20eff2b29cc09c4fe6271e501f1`

```dockerfile
```

-	Layers:
	-	`sha256:d9c59c5df0f7c39ad38ab2dbc4175966c984994a89c1f236ba31cc8fe1aed2fb`  
		Last Modified: Thu, 05 Jun 2025 23:22:22 GMT  
		Size: 11.3 MB (11270688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb499ab1e5a1cbc42e79fb1160c724f54fd228e61c10ba396a8b163ccdf5068a`  
		Last Modified: Thu, 05 Jun 2025 23:22:23 GMT  
		Size: 22.4 KB (22421 bytes)  
		MIME: application/vnd.in-toto+json
