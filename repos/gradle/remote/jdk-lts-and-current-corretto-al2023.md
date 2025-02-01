## `gradle:jdk-lts-and-current-corretto-al2023`

```console
$ docker pull gradle@sha256:d512374cd524c325b2088c5cff950c52d9818e47e8c379ef14efd556e6f35563
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:59533cf8d17da83f51f64df61cf9f329d38f2042e044ae86eb2a2354e2e9571f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 MB (595109550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fccd7af7a520e367532690d89ca482bd18502c5e58a3022f0ee75a361dd46eb`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:a2e8122f4c852d604a3ff5e6650100665488cf1de3c06e5533116d32d5aabe55`  
		Last Modified: Wed, 29 Jan 2025 02:05:37 GMT  
		Size: 53.1 MB (53149711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e6ebbd0576c9eb03a607a06c134baf8acfa090a9d5a17ec3633bd501bc6bf0`  
		Last Modified: Sat, 01 Feb 2025 01:09:00 GMT  
		Size: 169.8 MB (169754229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5433b778cf2eb1c09d8dd207cd09ceb8d56517a50e4e87696c925fb880aeb1ef`  
		Last Modified: Sat, 01 Feb 2025 03:08:54 GMT  
		Size: 163.5 MB (163481778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05c68358270cfc6017cb6d34b1ae83c5682fa70543908fa4a502a5d1ffdfa92`  
		Last Modified: Sat, 01 Feb 2025 03:08:52 GMT  
		Size: 72.1 MB (72111262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401902778de6d952263c403fd081595db6b0270a2f56b5382a831c3701975577`  
		Last Modified: Sat, 01 Feb 2025 03:08:49 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911942bd941ab12ce1d106f8884924d2fe0cde3c7e88a01e4ebc0aef18d6632e`  
		Last Modified: Sat, 01 Feb 2025 03:08:53 GMT  
		Size: 136.6 MB (136610781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:78cb74778df33ba5ea16b8b56731353090c694651333de4e82eae162a41bc614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10926012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe062aa8354465cf4a1566812aa477067250202001f543bb28bfa81e83160aa`

```dockerfile
```

-	Layers:
	-	`sha256:e8743322af1fd8447be95c3bacf1453976c81fb4e393b49d11cfde1f61e6cbd6`  
		Last Modified: Sat, 01 Feb 2025 03:08:50 GMT  
		Size: 10.9 MB (10900374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ec5d1fc3a32c6e2d17eb4e5509aabe5cac0318c896d9e9c8f5a78b48da0e2a3`  
		Last Modified: Sat, 01 Feb 2025 03:08:49 GMT  
		Size: 25.6 KB (25638 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:38e9adf9ca61e3e9e7969ec10fe414b6c9de9ec1087664381fc90fd234727c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.3 MB (590310631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0609cd43a8d591d0239b8fe7e06d7ea28d6a28b3bdaae1e07f1e30996f554ab9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:523a6b03095ed77c021e90dd9cc9c96374240d01b0165f628a7a82b4d9acd585`  
		Last Modified: Wed, 29 Jan 2025 02:15:16 GMT  
		Size: 52.3 MB (52269024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717cd8a2d259b91c259ea0266dbaa44ed12cdca6ba2c12f085093811c3fa5a93`  
		Last Modified: Sat, 01 Feb 2025 02:23:35 GMT  
		Size: 168.1 MB (168062282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7aebc7e70d448ebd1700a6417d3f9026396b31876244fc4de3dc6351adf5f`  
		Last Modified: Sat, 01 Feb 2025 03:14:42 GMT  
		Size: 161.6 MB (161571410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c98506e8e8f2a8814e544ae4557ecc1718b4333fe184eb62dd1ef75653dcaf3`  
		Last Modified: Sat, 01 Feb 2025 03:14:40 GMT  
		Size: 71.8 MB (71787347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9936881019f47782a0141b74b2fc366847b8fdc841a7975b14899e21e51d8f0`  
		Last Modified: Sat, 01 Feb 2025 03:14:38 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0564ca03db6acdc2cdc0bb4380e1e4c2b9d3af38ab9a5863591339e5dbaa39b3`  
		Last Modified: Sat, 01 Feb 2025 03:14:43 GMT  
		Size: 136.6 MB (136618779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e9ea3ff1bfad6e8e99a018363199f23ef427581e405571a0878f45ab84055e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10924137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cc957c54d0372f727b6a82c77b4776aa4ff4416f0b56fc948a0a2d822867cf`

```dockerfile
```

-	Layers:
	-	`sha256:e2783c8d62eb1d12baeb8fba289ce23f878a9a597daee3582c2c0bd0c72e0098`  
		Last Modified: Sat, 01 Feb 2025 03:14:39 GMT  
		Size: 10.9 MB (10898195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60e6429560b0cd5c5c43db7d4a51f8fc3f89c783d7a7a4c86650d471d92640b`  
		Last Modified: Sat, 01 Feb 2025 03:14:38 GMT  
		Size: 25.9 KB (25942 bytes)  
		MIME: application/vnd.in-toto+json
