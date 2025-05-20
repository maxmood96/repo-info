## `gradle:8-jdk24-corretto-al2023`

```console
$ docker pull gradle@sha256:4f497bdf9ed5ae7170fa4f833cbdd63ce24ed0d8b392e29913e99b23fe2e9e99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk24-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:8892db9625b8ec3fd8c1494e5e5d36a2e7458555161a7eff631a2aa02f52706b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.7 MB (450683708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd6e769e5a7af3abd452d38e2d90e7a4afafec112f8622d7f86bd24cae75c5f`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
COPY /rootfs/ / # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
ARG version=24.0.1.9-1
# Sat, 26 Apr 2025 01:26:29 GMT
ARG package_version=1
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Wed, 14 May 2025 01:42:44 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62dbbf3c08e9d1517a47b48f3a2d5a2957390e20d36f17ce3f450b6179adbac`  
		Last Modified: Mon, 19 May 2025 23:37:20 GMT  
		Size: 187.2 MB (187184906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f558371e66d2223832c7d7e735f95cb7bf9f507cff6ff37983c056e5c87e3f`  
		Last Modified: Mon, 19 May 2025 23:47:13 GMT  
		Size: 72.4 MB (72432970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e98faab13635fe12df034a929bd31291a75ff0392f03da845d437aa99d2ae35`  
		Last Modified: Mon, 19 May 2025 23:47:11 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b07c1e064d5735307c405e345820a43bfcbbb732e7d2b1f0f9f87553ba85b28`  
		Last Modified: Mon, 19 May 2025 23:47:16 GMT  
		Size: 137.4 MB (137394549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7377a4718bb534565d474c5daa9d897039184bb1b6605eb0871fba8497772cfd`  
		Last Modified: Mon, 19 May 2025 23:47:11 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e32961540e7322a5648297a6b8f0eaa70243956041455f07b5c2f88eba53eede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10830154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:491658dffd848a0979899524795383ae10965e74e500eab7abc38135ebd23c9a`

```dockerfile
```

-	Layers:
	-	`sha256:cc1e534a3a0a686bf834b042ceaec1ea79dbb53363601fb4fcd4a27b7b9f37dc`  
		Last Modified: Mon, 19 May 2025 23:47:11 GMT  
		Size: 10.8 MB (10810253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e0b6c90888a9a6b3817cb8344fceb2bce74c7ebe4783b595d8bad6938b6ae3`  
		Last Modified: Mon, 19 May 2025 23:47:11 GMT  
		Size: 19.9 KB (19901 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk24-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1c958e43896895e2fbcdaff32d73adbfdd9ef64173ea2d5157343c04deea7833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.3 MB (447282523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4643652d1ae68b6dc311bfcc9cd6e9461be046aba3c24af020987a4a12e5872`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
COPY /rootfs/ / # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
ARG version=24.0.1.9-1
# Sat, 26 Apr 2025 01:26:29 GMT
ARG package_version=1
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Wed, 14 May 2025 01:42:43 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606c71bde4a7d05e0626f9b64fb3e0bc776c63157501c509a656a16ad481691`  
		Last Modified: Tue, 20 May 2025 00:04:05 GMT  
		Size: 185.2 MB (185232892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09828004e241de6c06ee27ed31e76d014e4989712b8ea4bb7d83f2089afbd9f4`  
		Last Modified: Tue, 20 May 2025 00:31:40 GMT  
		Size: 72.0 MB (72028083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b87e3a51671ed5f763baf4a9e8350e2cb2f5b423583ec61c108ccc17c61fbc`  
		Last Modified: Tue, 20 May 2025 00:31:38 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ec617de517cf3fc9687895dd3a5b8b0490a04b2c8719a8758c9b901a3f771`  
		Last Modified: Tue, 20 May 2025 00:31:42 GMT  
		Size: 137.4 MB (137394599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d340a3da355bca99cd9a5bc9dac98f78b2c6fdb8072846d8b6477c6df62286ae`  
		Last Modified: Tue, 20 May 2025 00:31:38 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:bc8baf036bd28f4e8a73ddc9fc78dd2553e38f74c4375a206ab698afed94afc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10829364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b75fc771f1aa55b2a93f65304a36d3011cb172b41800f2d5a3b75691b73b752`

```dockerfile
```

-	Layers:
	-	`sha256:895bb9b5812b0016e5d3dcec05c143be1b1505815760a7312cbd621b45fbbcb4`  
		Last Modified: Tue, 20 May 2025 00:31:38 GMT  
		Size: 10.8 MB (10809266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c37a422de30b44c3c36409c15e2c1e9a7e19faf786a8ee39bbe193f54d420884`  
		Last Modified: Tue, 20 May 2025 00:31:38 GMT  
		Size: 20.1 KB (20098 bytes)  
		MIME: application/vnd.in-toto+json
