## `gradle:8-jdk21-corretto`

```console
$ docker pull gradle@sha256:58b23ec1d2829b725fa382b4ae0f70c7aeb3306d40db932915878205a156e36b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:22c3a66685ba61eb4c7050b281d45b3ebf4c0e978639bf922128c5b576281b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447650978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047ba33d16ff259b8bd3dcdfdcbb2411b2f007cd386268343785a466989e2697`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:01 GMT
ARG version=21.0.9.11-1
# Fri, 14 Nov 2025 02:17:01 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:17:01 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:17:01 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 14 Nov 2025 03:13:55 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:13:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:13:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:13:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:13:55 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:13:55 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:13:55 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 14 Nov 2025 03:13:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 14 Nov 2025 03:13:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:13:58 GMT
USER gradle
# Fri, 14 Nov 2025 03:13:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:13:58 GMT
USER root
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea90e0b86912d07adb758db1884d17f649cd6e3ce55ec3eff308135c598e2d`  
		Last Modified: Fri, 14 Nov 2025 03:12:58 GMT  
		Size: 170.2 MB (170193178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a08e2c06a4e42f8cf8c415d0aa7715d31052e3abcc3a3a51820ef0b8034535`  
		Last Modified: Fri, 14 Nov 2025 03:14:45 GMT  
		Size: 86.0 MB (86029307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1cb16de8e8a3254770ab7f6a26206b745030157bdbde8fa6b10229d96dc666`  
		Last Modified: Fri, 14 Nov 2025 03:14:38 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059066a3843f911a719705341bf9a4b5d9dacbb4465bd3fe7fcfee71b5d30f1f`  
		Last Modified: Fri, 14 Nov 2025 07:25:59 GMT  
		Size: 137.4 MB (137395195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9240961c9754f6a8726f39e52cd85f68ed30951c0cfce853b419567c937cfa7`  
		Last Modified: Fri, 14 Nov 2025 03:14:38 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:91a830e9829e1db2bda5196f1125f25bfa2ad1ad613f5b9280972de30914502f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1029778e6198217120b8b09fe487447f73254e7ba2a5b0e1058f2ec0f400bb`

```dockerfile
```

-	Layers:
	-	`sha256:d8d7966214249f9c4bb1e12df5bed9ebdc9221192871068186108153cbb55161`  
		Last Modified: Fri, 14 Nov 2025 06:20:59 GMT  
		Size: 11.3 MB (11342256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd147464462499cb06b7b473450a9911a08af8ae394b186f1724dc1f35bcd49`  
		Last Modified: Fri, 14 Nov 2025 06:21:00 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c4c63a923f19a4e8985fb4cd3f6c40c3a5aa7f6851959246435f5a1f8c6ce84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444318506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d666d611c1314e657e281a2b51a6f0df79622c3d711af1da26c4120da4446e6`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:19:58 GMT
ARG version=21.0.9.11-1
# Fri, 14 Nov 2025 02:19:58 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:19:58 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:19:58 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:19:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 14 Nov 2025 03:14:09 GMT
CMD ["gradle"]
# Fri, 14 Nov 2025 03:14:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 14 Nov 2025 03:14:09 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 14 Nov 2025 03:14:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 14 Nov 2025 03:14:10 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 14 Nov 2025 03:14:10 GMT
WORKDIR /home/gradle
# Fri, 14 Nov 2025 03:14:10 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 14 Nov 2025 03:14:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 14 Nov 2025 03:14:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 14 Nov 2025 03:14:12 GMT
USER gradle
# Fri, 14 Nov 2025 03:14:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 14 Nov 2025 03:14:13 GMT
USER root
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb278807b7599e6451a57100c14ec259294cbfc0994bc81d5d0797784a723b5b`  
		Last Modified: Fri, 14 Nov 2025 03:13:39 GMT  
		Size: 168.4 MB (168449435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca5ad277e86820e4db160b18c5ecf9f336ed111611c3a17bff8f168175ef104`  
		Last Modified: Fri, 14 Nov 2025 03:15:05 GMT  
		Size: 85.5 MB (85535999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae97d36d02b9c22f3f19b2b6b0278b5187e08ac1d511855d2fd84e7bee34a014`  
		Last Modified: Fri, 14 Nov 2025 03:14:55 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61fb078aec83599dafc1d30b9efd7c9ffce90e0dbf14c896517ab902031e945`  
		Last Modified: Fri, 14 Nov 2025 08:28:08 GMT  
		Size: 137.4 MB (137395193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89715518cdf8ae926c74fb26392f1436949a49f1cf66fb74aa723ab6f6cc056a`  
		Last Modified: Fri, 14 Nov 2025 03:14:55 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:67fb3fc9e346c76942b332ad8ea5192c8078c21ca6994f14814254e3b9903ec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11362288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4455221a94333e5d1ec3f995dafd0f57dd3c4c124299b334291613320bb36b59`

```dockerfile
```

-	Layers:
	-	`sha256:5e46fa15603e88deffbc8aab64b5ae4de8bf06ffdcde32292525c65fbcc1b2e7`  
		Last Modified: Fri, 14 Nov 2025 06:21:09 GMT  
		Size: 11.3 MB (11341234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27471292609ffaea54b81ac582312c3a39d3bfcfc907808e91c0100f487859a`  
		Last Modified: Fri, 14 Nov 2025 06:21:10 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
