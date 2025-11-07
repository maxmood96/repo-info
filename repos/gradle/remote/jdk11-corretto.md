## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:dd7be172cd9625ab093dc5e7ba510d11f8cf638ae028b34b284fb8e8e580d675
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:588b2af3baecbffa4a125bf21a338ff1c285b4cd948ebb7da4ce3bd4494828ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.4 MB (430421113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26004e4394f25b56eebc9811453d6dddb6212f291e1dc11c5f3bc809ae703238`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:11:58 GMT
ARG version=11.0.29.7-1
# Thu, 06 Nov 2025 23:11:58 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:11:58 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:11:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 07 Nov 2025 00:12:24 GMT
CMD ["gradle"]
# Fri, 07 Nov 2025 00:12:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 07 Nov 2025 00:12:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 07 Nov 2025 00:12:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 07 Nov 2025 00:12:25 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 07 Nov 2025 00:12:25 GMT
WORKDIR /home/gradle
# Fri, 07 Nov 2025 00:12:25 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 07 Nov 2025 00:12:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 07 Nov 2025 00:12:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 07 Nov 2025 00:12:27 GMT
USER gradle
# Fri, 07 Nov 2025 00:12:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 07 Nov 2025 00:12:28 GMT
USER root
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b473a7250c0332e852acae35168b4b0630488129fbb2f0d4d6bc1bf0401b8e`  
		Last Modified: Fri, 07 Nov 2025 00:11:58 GMT  
		Size: 153.3 MB (153344907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e0120849ac065d1ecec1ee7a9cd173e0d5011779e6f1317c2602785760d1b0`  
		Last Modified: Fri, 07 Nov 2025 00:13:19 GMT  
		Size: 85.6 MB (85623917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd79017bd66f959c46ad265dc1a3d70ffc703497fa2c41bf74ebb4df4fe50b1c`  
		Last Modified: Fri, 07 Nov 2025 00:13:09 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f43b9535fa09593b19b734f7ffad169a47aaad13cc41d25eeaafcc112117b3`  
		Last Modified: Fri, 07 Nov 2025 05:56:05 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e7d859608af124ac50fa5a4e74d99f3b8b50504c08418b7f5108de69ee8072`  
		Last Modified: Fri, 07 Nov 2025 00:13:09 GMT  
		Size: 54.9 KB (54912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:2f68a921698f003b9b5133a53d50f22558b0d005c46f92334eaf6ace10a6c385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11366135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753800f30b07a386ffeeec0540a5f5514f668e1a63b416c647f5dd5448b3f0b3`

```dockerfile
```

-	Layers:
	-	`sha256:5451b3b22723e32a1529d76eca0e736e8ee82d0fa5be66b48c72195a874ded38`  
		Last Modified: Fri, 07 Nov 2025 03:20:19 GMT  
		Size: 11.3 MB (11344612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d219a4149560eb411cbcbbac258cd4f48a39c7c5c4cb475f3da7f06cdd6ac1`  
		Last Modified: Fri, 07 Nov 2025 03:20:20 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1603feb10e55e02214c7732c92eb8e45bd5458e901ef7dd2d90247f3ab9826c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427415252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748c15d293f2fe66c98ad0dac7d15128e81aefed313d5ddc1f20a0522f6d590f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:29 GMT
ARG version=11.0.29.7-1
# Thu, 06 Nov 2025 22:13:29 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:13:29 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 06 Nov 2025 23:12:39 GMT
CMD ["gradle"]
# Thu, 06 Nov 2025 23:12:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Nov 2025 23:12:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Nov 2025 23:12:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Nov 2025 23:12:39 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Nov 2025 23:12:39 GMT
WORKDIR /home/gradle
# Thu, 06 Nov 2025 23:12:39 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 06 Nov 2025 23:12:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 06 Nov 2025 23:12:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Nov 2025 23:12:42 GMT
USER gradle
# Thu, 06 Nov 2025 23:12:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Nov 2025 23:12:43 GMT
USER root
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f1158d8b36acddc8839ac2d61ff7da04401b085f3c33c4996bbdc4d1e0ea8a`  
		Last Modified: Thu, 06 Nov 2025 23:12:11 GMT  
		Size: 151.9 MB (151892114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b856fae97d3adb67f5eea9c2652184e32d45c4467ed1c6847ae3e75cbc8bc`  
		Last Modified: Thu, 06 Nov 2025 23:13:28 GMT  
		Size: 85.2 MB (85165046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af2f5e5a1716a6ad1050cbff66eb829ac9d8f6bec80ed241b73cb4e6f161ce`  
		Last Modified: Thu, 06 Nov 2025 23:13:22 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8fdd1956dfc50b4ce025ec84fef50833350f313d7de1a55307067977cd4a64`  
		Last Modified: Fri, 07 Nov 2025 05:56:07 GMT  
		Size: 137.4 MB (137395194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd4ad51bf59f1a60c5ba972aed75bc36004718bb0e207b24836ec39b8d9bcb6`  
		Last Modified: Thu, 06 Nov 2025 23:13:22 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:91a3a990c75a4a25daaba61f7cf32fa6b2ddddfa6cbeedd1241a05eed748da85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11366175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de8447eefb44cd9c76990661c553689db3a36ae6abd1fa16714ba965f940145`

```dockerfile
```

-	Layers:
	-	`sha256:f107a0363344e2a664e02daab14ef7763cfde75fcf6a1b90182c1a7c97876663`  
		Last Modified: Fri, 07 Nov 2025 00:20:20 GMT  
		Size: 11.3 MB (11344455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e893c983caa2eed2222bd598c2037a4767e3eb52cbc2e627bebc813af7c038a8`  
		Last Modified: Fri, 07 Nov 2025 00:20:21 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
