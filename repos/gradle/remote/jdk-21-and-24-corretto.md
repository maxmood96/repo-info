## `gradle:jdk-21-and-24-corretto`

```console
$ docker pull gradle@sha256:ec50b7c75610356207865ef258539ba8c48ebcb6c94f8a46fef4fcce5331dd0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-24-corretto` - linux; amd64

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

### `gradle:jdk-21-and-24-corretto` - unknown; unknown

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

### `gradle:jdk-21-and-24-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:00345c04c8234840aa9d01db9293f6df4e33e37ec5c54a7c061a3c701f457571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.4 MB (601371828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d974fe10af93deb716cf1b7dca87eaf35ef3cc5c56f3cdc977e08d6168ca060c`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:28 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:28 GMT
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
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636d528c330bfbf25f01c47594e400fbdd346f49427a00980cb3647a53fc073d`  
		Last Modified: Wed, 16 Apr 2025 00:16:57 GMT  
		Size: 168.2 MB (168216008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d041267b8dbb42dd916652462cee20c24d48f1958b28c7cbb1f915093f7a61`  
		Last Modified: Wed, 16 Apr 2025 01:10:23 GMT  
		Size: 171.2 MB (171171250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b9cb933c8aba174fa1bdfe9fcd40f2e78c0ff7d3a875971669c2274d2a15d7`  
		Last Modified: Wed, 16 Apr 2025 01:10:19 GMT  
		Size: 70.0 MB (69971062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3b2020da3f9fe547910f2c5d3b8feb44326c25d1a2b2cd44f169a84d3e444a`  
		Last Modified: Wed, 16 Apr 2025 01:10:16 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2defb44f270da83372c7114783afe6ad2a97d0b3a4b2d98f9d6f33a2edb15c`  
		Last Modified: Wed, 16 Apr 2025 01:10:20 GMT  
		Size: 137.1 MB (137050711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b6dfc29f3308d1439295d2832e5c7454b353aef5457ba6a0bf6b54cd31ae15c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10941188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e133fe7a3680b4e07daf8836affcde8c7eae5bdba8c5bb2677a4950dfef1d25d`

```dockerfile
```

-	Layers:
	-	`sha256:eb5241d8580a774ab4fcfab78e73b4cc123cac567f63844e27eb5615256b1ae1`  
		Last Modified: Wed, 16 Apr 2025 01:10:17 GMT  
		Size: 10.9 MB (10915249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6857672c94f2fb765de6deeb7d1ccb17cea522c45beb66604990a9a5ff7485e5`  
		Last Modified: Wed, 16 Apr 2025 01:10:16 GMT  
		Size: 25.9 KB (25939 bytes)  
		MIME: application/vnd.in-toto+json
