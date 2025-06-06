## `gradle:jdk24-corretto`

```console
$ docker pull gradle@sha256:d9b23cf98051db8357f5bf3a39c449c932bcebc4bf3b038e680f7e5b5b7208d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk24-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:69a6d79c083c7419ba23b3966140b54d9deea3e1504f0b7b05ae2843770b7fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.9 MB (461909485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e43554293cf25d0f55bbba4a5f1e0ef21e65104de22d21c482855759e268c74`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
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
	-	`sha256:c62dbbf3c08e9d1517a47b48f3a2d5a2957390e20d36f17ce3f450b6179adbac`  
		Last Modified: Mon, 19 May 2025 23:46:03 GMT  
		Size: 187.2 MB (187184906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca123a47ad1559dd371f49f79bd71f450f169612ab177dcf26462e1b66364b9`  
		Last Modified: Thu, 05 Jun 2025 20:02:23 GMT  
		Size: 83.7 MB (83657789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb14fabfa196db8f2a23d1410fd90235d5672709be0df6b3553417243dc1fc8`  
		Last Modified: Thu, 05 Jun 2025 20:02:16 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0a8508ea1eee095914dc8af7998efa5927ca814008819fd6b679b98af103d0`  
		Last Modified: Thu, 05 Jun 2025 22:35:45 GMT  
		Size: 137.4 MB (137395506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17ff12998f058b834e23b0133d6881fa7ef38f1052840bc3dce4b9d84c866de`  
		Last Modified: Thu, 05 Jun 2025 20:02:17 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:6c8d921ddda9b5e58c3baf81e2b16f28b5fe30997c9cc2ab6708733a357c1738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11304188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bba493e521ae48ede2774329b8da7edc3f4f0c0374cf83fd7d2b79f12f7ae57`

```dockerfile
```

-	Layers:
	-	`sha256:f2787ee1bff0bcd411f3e1fcbedcb99187a47d14e9a28b5b3626627530517d6c`  
		Last Modified: Thu, 05 Jun 2025 20:21:46 GMT  
		Size: 11.3 MB (11282607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d5d12ded4b2914a469578931eae885ed406d07ad9e719a0176c8cbc21a3b76`  
		Last Modified: Thu, 05 Jun 2025 20:21:47 GMT  
		Size: 21.6 KB (21581 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk24-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d9e3e8ee61e95b3c4beb8fe0873bb9eaa4b7370ac5759ef3cc81c582f9d8b016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.5 MB (458484545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a61768282a21f336aef77a37ab071d571ed3c99afa957dae9cd1225b37b6b9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
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
	-	`sha256:8606c71bde4a7d05e0626f9b64fb3e0bc776c63157501c509a656a16ad481691`  
		Last Modified: Tue, 20 May 2025 07:19:50 GMT  
		Size: 185.2 MB (185232892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b930de29459826d11666af4e4c3e37faf95cc3a27ac035a5ab3b5669f3cb4702`  
		Last Modified: Tue, 03 Jun 2025 14:26:54 GMT  
		Size: 83.2 MB (83229193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3246d2bb3ade0125f375e3fe09ce63011e48f397ead0f4526b5fe2b8c8afb0c4`  
		Last Modified: Tue, 03 Jun 2025 14:26:32 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc955c5877114542061fc4e96b86294e86eabef53db389ccd5bca0dfb851e46e`  
		Last Modified: Fri, 06 Jun 2025 02:12:03 GMT  
		Size: 137.4 MB (137395508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bf276dbbe713f8a28c3821dbc86ff6040ad7d8b62429036d000fe81d5f4f2a`  
		Last Modified: Thu, 05 Jun 2025 20:26:38 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:fa07a844c8b5c421742da9256b1909b647389cabd3ff02bf716a019603a0ea85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11303399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9feea774f262bb389bbc5d94e9b8507d24330b1c5d418d9a53c0161f3fae02b`

```dockerfile
```

-	Layers:
	-	`sha256:26c6aa039faf392bac8e8b6c06aab22c12ab796c28e5a10544246644b763443c`  
		Last Modified: Thu, 05 Jun 2025 23:23:02 GMT  
		Size: 11.3 MB (11281620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0247bdad49d07c09095fe3b034e6e229667cde3151073481f303f32e73d46bbe`  
		Last Modified: Thu, 05 Jun 2025 23:23:03 GMT  
		Size: 21.8 KB (21779 bytes)  
		MIME: application/vnd.in-toto+json
