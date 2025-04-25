## `gradle:jdk-21-and-24-corretto-al2023`

```console
$ docker pull gradle@sha256:16c876a43793e347e6ef173150609b5c96cd455bea7290c9a40b30e37f1eaacf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-24-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:5e1e531af9c09dc0a3776a39f998bac2acd7e735d0303a92fd6a911b87d054f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.4 MB (606433814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:489ed54dbe25cd3f207208d1b937a16f1b7d2d4aafbe724b11b6e85b4c1dbc03`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 15 Apr 2025 14:24:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:24:24 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 14:24:24 GMT
ARG package_version=1
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 15 Apr 2025 14:24:24 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:1cf9fb914831ab202ad1756fe44227d7c88c49394a5cc9749ad863e76989673c`  
		Last Modified: Thu, 17 Apr 2025 22:49:09 GMT  
		Size: 55.9 MB (55906521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e99dbc572ddbd1143236e4dc8332db0fd4b797dffd1975ef26f5286d21177c`  
		Last Modified: Thu, 24 Apr 2025 20:08:25 GMT  
		Size: 169.9 MB (169917710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b4d0940a37d5c1999d4223bc8649fe04c7fbf0c32a909522fb14d9cdf69c98`  
		Last Modified: Thu, 24 Apr 2025 21:08:56 GMT  
		Size: 173.1 MB (173078809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a9229420e6a1a4695f77df1f7ca8225933c432266a2df6e2d858e99eac6f91`  
		Last Modified: Thu, 24 Apr 2025 21:08:54 GMT  
		Size: 70.5 MB (70488283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc13a512b01a5b93563784f4092f218edfc11f8055a2e4d5abe38d5ccf2ec573`  
		Last Modified: Thu, 24 Apr 2025 21:08:53 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6374c1198d87ec4c72d00b35ce71d94db26092d66a0309c738996a553477cf5a`  
		Last Modified: Thu, 24 Apr 2025 21:08:56 GMT  
		Size: 137.0 MB (137040702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:6de615f75ece88b07f3c678c15b22fd7dd0a880610c30cdd6a75a8bdcb3f5058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10942427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bcbe99cd6f4885071921483e4e32a0ca439607b620d58710bdb4947d595b90`

```dockerfile
```

-	Layers:
	-	`sha256:57ae1e8c6ae7e32054d15d3ecfc44fdd46250efdc1e083d0352413cf467502c8`  
		Last Modified: Thu, 24 Apr 2025 21:08:53 GMT  
		Size: 10.9 MB (10916791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52131e6d7da27262323bd72223fc8bdfe5cb4db4fc367cc2b93002ee6a406bbf`  
		Last Modified: Thu, 24 Apr 2025 21:08:53 GMT  
		Size: 25.6 KB (25636 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-24-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8c479607895ed6e17614b8760f57b3ed68c5234c062911e51cb8c02e7ba9ea5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.3 MB (601348022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe2c8e133bfc05d2a9f23121559fbe4660a9bd340a81f7feb713cdbfbf2d440`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 15 Apr 2025 14:24:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 14:24:24 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 14:24:24 GMT
ARG package_version=1
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 15 Apr 2025 14:24:24 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 15 Apr 2025 14:24:24 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 15 Apr 2025 14:24:24 GMT
CMD ["gradle"]
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 15 Apr 2025 14:24:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 15 Apr 2025 14:24:24 GMT
WORKDIR /home/gradle
# Tue, 15 Apr 2025 14:24:24 GMT
ENV GRADLE_VERSION=8.13
# Tue, 15 Apr 2025 14:24:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 15 Apr 2025 14:24:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:3851c1e87439f4d250c3c0908923968a64dd743e1e5cfc05b798a52dc5d1e215`  
		Last Modified: Thu, 17 Apr 2025 22:49:07 GMT  
		Size: 55.0 MB (54961479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e929c1d40d3411c88ee7ec677ac2d0139c209d465db1eaaa6f5d8bc9003a9a0`  
		Last Modified: Thu, 24 Apr 2025 21:22:26 GMT  
		Size: 168.2 MB (168216046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb1db69b6c551b703b577ac7e5fc361c2cd4d6801b58cd981b0af56de864775`  
		Last Modified: Thu, 24 Apr 2025 23:40:09 GMT  
		Size: 171.2 MB (171171247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8ba64fdaba5cd7a38d0c4c199ebfc9a44668ba45c99a9fe852f93f2d5d32d7`  
		Last Modified: Thu, 24 Apr 2025 23:40:04 GMT  
		Size: 69.9 MB (69946828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cdbe71ff988f3a09bb167d9fc3d8a2d2c48054315dbb645c0007f7e8c73d15`  
		Last Modified: Thu, 24 Apr 2025 23:40:02 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1db5166a0014afa07c37a3b573e5a272e38b7401253128e926fdd826f42f11`  
		Last Modified: Thu, 24 Apr 2025 23:40:06 GMT  
		Size: 137.1 MB (137050632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:74f9e23e9f8b024425e8fae6e29bdf19b68704dc1eb9d4a7fa021b0f8258c5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10941189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a2a1bff5720eedf1c8cfa171908ac2dfec86f8c633f39caa086fdebb39b710`

```dockerfile
```

-	Layers:
	-	`sha256:51361efc365627553eb9a1c737e2eec1e53817be9ce238f6ff5bac49799e1672`  
		Last Modified: Thu, 24 Apr 2025 23:40:02 GMT  
		Size: 10.9 MB (10915249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e047638e0bf78ce9c6c7c9df6dfbd0ea8a188807d6f8238493de4e305eec8948`  
		Last Modified: Thu, 24 Apr 2025 23:40:02 GMT  
		Size: 25.9 KB (25940 bytes)  
		MIME: application/vnd.in-toto+json
