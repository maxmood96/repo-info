## `gradle:9-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:a8909957f52005de272cf1ec11b9b5df2029811453ca95a06d8d81d4f4da96cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:6cc3f3a8ce2d4cf2522d8f29e8a744909d2a3f9e1c4281baa63a99083cd4fa32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.1 MB (448095952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a678de474c12062ff64fb0c7c71a082c156ddda34dcb9ceaef88b7d7dc9c659`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:01 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:34:01 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:01 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:01 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 11 Mar 2026 19:12:55 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:12:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:12:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 11 Mar 2026 19:12:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:12:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:12:56 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:12:56 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 11 Mar 2026 19:12:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 11 Mar 2026 19:12:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:12:58 GMT
USER gradle
# Wed, 11 Mar 2026 19:12:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 11 Mar 2026 19:12:59 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f515facfbc58fdfaa9cdcbd4b5a55791c80be6edda4df3bb9183ca525b464ed`  
		Last Modified: Wed, 11 Mar 2026 18:34:23 GMT  
		Size: 170.2 MB (170192431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578485d2ff6139a37d6b7b4504540002a93c9c6803c8a7c920f04ba671aa271e`  
		Last Modified: Wed, 11 Mar 2026 19:13:30 GMT  
		Size: 86.1 MB (86069974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581f4219cddc4bd81efb23e2a14a232dda8b4cb590dae48c9f5d5a87e878a75f`  
		Last Modified: Wed, 11 Mar 2026 19:13:23 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de24fa1861cb53edf0b4aca66ad3315555492db364716ce7a33ba8f1e251d584`  
		Last Modified: Wed, 11 Mar 2026 19:13:28 GMT  
		Size: 137.8 MB (137773157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b88b90a51c9b7165980cf81470c39429d982ea58354b2d3de0651b95a51bccf`  
		Last Modified: Wed, 11 Mar 2026 19:13:24 GMT  
		Size: 25.6 KB (25618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:4b1a646732abcf856de4caa53d6d1cf35a795bce515d78f01fd9aa4ec494a99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11350409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ad57966f3ed5f90424ee6f0a6aa129c37034ffd62715f1ded90f5ca8f39cbf`

```dockerfile
```

-	Layers:
	-	`sha256:734e23034b3a28327d8e4396388b698c2b4e2eb0a559833fceff061f39cef0d9`  
		Last Modified: Wed, 11 Mar 2026 19:13:24 GMT  
		Size: 11.3 MB (11328758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16866ba39c4608853e7580dbf83240311982a2cdfbeb83718a49688957d2cda5`  
		Last Modified: Wed, 11 Mar 2026 19:13:23 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f8173364104bba1cfbcc994f9dacc797b8c68b31e3ed6776438f58450f1021c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.8 MB (444754081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f529b84adbafe99d95234b34f453cf01eee7f27f9bcbeb6adf1230c54e41e987`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:49 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:33:49 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:33:49 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:33:49 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 11 Mar 2026 19:12:53 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:12:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:12:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 11 Mar 2026 19:12:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:12:53 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:12:53 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:12:53 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 11 Mar 2026 19:12:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 11 Mar 2026 19:12:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:12:56 GMT
USER gradle
# Wed, 11 Mar 2026 19:12:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 11 Mar 2026 19:12:56 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d30746b1d1a0fa8e3ef2fe5cc5ec2c6c146413028b9dd25386bd91e4b836e`  
		Last Modified: Wed, 11 Mar 2026 18:34:14 GMT  
		Size: 168.5 MB (168466825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4e4d321ea8aa4c56b2ff152d07815a3d81c7bc883783ea23d9a1520f428455`  
		Last Modified: Wed, 11 Mar 2026 19:13:28 GMT  
		Size: 85.5 MB (85541711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5111702108bbcdb15c23827fd119f436c0f92426b52dbd0e6510a8a132bbe5f2`  
		Last Modified: Wed, 11 Mar 2026 19:13:24 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf29771ed18cda19d852091fbd52c110acd43e14474e338259a31d23871e8c7`  
		Last Modified: Wed, 11 Mar 2026 19:13:29 GMT  
		Size: 137.8 MB (137773159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7a1034cffaee70338102dcb7d013397b10f3c53436a036a4ffc6110019ea21`  
		Last Modified: Wed, 11 Mar 2026 19:13:25 GMT  
		Size: 29.3 KB (29333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:51d5512ef0985d720bc4ca46ab311ab8bfe1899eb126d872e1842892da0580e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11349608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e794f5592d66239e04b6e12d421bd1af96ae2713418509faf64b15a16cd9236`

```dockerfile
```

-	Layers:
	-	`sha256:f6cc257d4f0600b52800b478696d06dba561472ec8a7e091e5e2ae28acf35b81`  
		Last Modified: Wed, 11 Mar 2026 19:13:25 GMT  
		Size: 11.3 MB (11327760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ccdb7c99653af19f7907ac28a3a1e744e93eed78840bba32ef661e87500c7e`  
		Last Modified: Wed, 11 Mar 2026 19:13:24 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
