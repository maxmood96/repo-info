## `gradle:8-jdk-21-and-24-corretto`

```console
$ docker pull gradle@sha256:d533b8a7f11ff60e1653897df6b23550b3d6e2a2f87bee25fbb4ca5231f09f9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-21-and-24-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:27aa2dd61ffb18ef5dfc126326a9862d1ae405634b891bd038cba652769ce59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606451592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1907284ab7fde44e004435b1ed73027b1090deceb21be94e8c93d4e6b5b1ff76`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:23 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:23 GMT
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
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec1e3a2d6aab5829276e8f0cf7cd601be82c37d69ed45fb5d0b2277f45320b8`  
		Last Modified: Tue, 15 Apr 2025 23:56:03 GMT  
		Size: 169.9 MB (169917730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912efe591cf1f5d01c7fecc3c978c005d3a20c5c7078a904d165d32f31d0da9c`  
		Last Modified: Wed, 16 Apr 2025 00:08:53 GMT  
		Size: 173.1 MB (173078853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47bb880f4a3fae59c06fc6e588847b8cf0e66d0c77820976bf2aa91eb6ad834`  
		Last Modified: Wed, 16 Apr 2025 00:08:52 GMT  
		Size: 70.5 MB (70505494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b126204479b259b0ee8abed2767046a1f66e492e5c91728fb4b539a6cce2821`  
		Last Modified: Wed, 16 Apr 2025 00:08:50 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874c1b919d39e61d074b94d59f44e272b41f97bf1a6de249cbb1dcf8b882e3cc`  
		Last Modified: Wed, 16 Apr 2025 00:08:53 GMT  
		Size: 137.0 MB (137040673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bfef54d750dccaba03d4adb63f137d6263137a20c645c94221c730baed0d6514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10942426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5980d5aaf2b2667bd12e136ea65791ac6360bb57070555aad43e4982e369944`

```dockerfile
```

-	Layers:
	-	`sha256:ceaab7e7c0c286c3a6dcd956861ade3822ecfd3743e62ffd2c061167a1c973af`  
		Last Modified: Wed, 16 Apr 2025 00:08:51 GMT  
		Size: 10.9 MB (10916791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514c6d234fde2faffca77765cf9fddbc929d1857d5462ab15206614cfc72c0b2`  
		Last Modified: Wed, 16 Apr 2025 00:08:50 GMT  
		Size: 25.6 KB (25635 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-24-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:173e6d3485068902aedd0b7263e2eb4bddecef7b0beea0b055369b0b95996681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.3 MB (601335147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccfa509588a772871af0c9d9b2ce4224334006793eb468a571b212cc1497b7`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 27 Mar 2025 21:20:39 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 27 Mar 2025 21:20:39 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["gradle"]
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 27 Mar 2025 21:20:39 GMT
WORKDIR /home/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_VERSION=8.13
# Thu, 27 Mar 2025 21:20:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffca6b39b82b7986bb48be82129ceb9f9a0067ab8aa14e908ea6a8bee317c1d`  
		Last Modified: Wed, 02 Apr 2025 00:33:14 GMT  
		Size: 168.2 MB (168169083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0de339e2bfc790afe7e642cba0b556c9b63a7219b3913c236b646b25418ee3`  
		Last Modified: Mon, 07 Apr 2025 20:22:42 GMT  
		Size: 171.2 MB (171181684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250977e2822e0854eba3e92568f98e226369e37dce24e14dadb5de78a95997d6`  
		Last Modified: Mon, 07 Apr 2025 20:22:40 GMT  
		Size: 70.0 MB (69970841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49630c85e079acecb316e0ec8c6701d77d850dea62e9804042f26ed1f83ebad`  
		Last Modified: Mon, 07 Apr 2025 20:22:38 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2846916cdf4a8552bce1613a5f3c7d7f8866137194cc6144ec4ed072b466eec3`  
		Last Modified: Mon, 07 Apr 2025 20:22:43 GMT  
		Size: 137.1 MB (137050742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a441b42a28bc71dbb35b6f6e7932879e16d549dd813c87ea29bafa16cba69245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10941175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f5a1f3df6c42b3b14795f576d63db557dcfd09818bad06f92cb1151bf1aa26`

```dockerfile
```

-	Layers:
	-	`sha256:61d5ab411cc6c3d24ee0730836e0ac8587f0e2bfafec21117f61dc04b0583370`  
		Last Modified: Mon, 07 Apr 2025 20:22:39 GMT  
		Size: 10.9 MB (10915235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f746ca807d28094e78d1732bff1016dcf302c486663382af2a9d52de7b09fca9`  
		Last Modified: Mon, 07 Apr 2025 20:22:38 GMT  
		Size: 25.9 KB (25940 bytes)  
		MIME: application/vnd.in-toto+json
