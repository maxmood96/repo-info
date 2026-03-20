## `gradle:jdk-lts-and-current-corretto-al2023`

```console
$ docker pull gradle@sha256:e7271afe02c79c73ab903938c54f3b9ac19595835325f77e27641a49e9e39a38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:aae7cd34ddcfc6dbaed878fdfc7fa44802cef587cdfc7d0d3ffb598783b8b7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 MB (467129064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0011077e0aa3f2f7446725b95412f24dab9b7ddfd82958c6dcf6564cf83ef3f`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:25 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:25 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:25 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:25 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 20 Mar 2026 17:12:15 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 20 Mar 2026 17:12:15 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 20 Mar 2026 17:12:15 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:12:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:12:15 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:12:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 20 Mar 2026 17:12:16 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:12:16 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:12:16 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:12:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:12:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:12:18 GMT
USER gradle
# Fri, 20 Mar 2026 17:12:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:12:18 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1899f99dbf61d2e92bf9bc374b2f4ec7c5b8a1687b8543b4ecc212164833f14`  
		Last Modified: Wed, 11 Mar 2026 18:34:50 GMT  
		Size: 189.2 MB (189186371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c9d941b677f123da9b3c20e5f4372f7dcf1d71f1db7310570b5fe3883a7d19`  
		Last Modified: Fri, 20 Mar 2026 17:12:49 GMT  
		Size: 86.1 MB (86073874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef83d7305149a3bf33155d98e910bebec421e1b1e37978eebe79f9643332a453`  
		Last Modified: Fri, 20 Mar 2026 17:12:46 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8c60370e80e30dfcf9b2a5a523e7e3d0d627c1f7c6430918d73c66be9ebb7e`  
		Last Modified: Fri, 20 Mar 2026 17:12:52 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf01f3a0b96013585c80dab561f22207a18d0cd8ce664edda892e4b0cb7fe7a`  
		Last Modified: Fri, 20 Mar 2026 17:12:46 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:289040eeb077808b7d94aa29cc34fb972dedbd4adb70c4394b572d8a7037ef7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542bb4bb84d16d63d47f72714d62f95b97f8cb48df12550a256b52ceab81f1d1`

```dockerfile
```

-	Layers:
	-	`sha256:674ee3ca98a190d233fc1c59764841e3e2bca9839cd64723e566f73956555396`  
		Last Modified: Fri, 20 Mar 2026 17:12:47 GMT  
		Size: 11.3 MB (11343297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68b9e2c22673906a7c6e9fd5b9057ff9bb890277ebec5b1b86dd5d28a5b6b9b9`  
		Last Modified: Fri, 20 Mar 2026 17:12:46 GMT  
		Size: 26.5 KB (26477 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:07089136688d0d3642846581faeaf5d6e463eeeb56b5e385dec6cff3bea9d2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463415229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd71e3969afc582b365463185ed5f3d2645e1ad7b4fd54c90c0eb06a09eb921`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:05 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:05 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:05 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:05 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 20 Mar 2026 17:26:58 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 20 Mar 2026 17:26:58 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 20 Mar 2026 17:26:58 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:26:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:26:58 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:26:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 20 Mar 2026 17:26:58 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:26:58 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:26:58 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:26:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:27:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:27:01 GMT
USER gradle
# Fri, 20 Mar 2026 17:27:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:27:02 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9ab420359a2ce38b24b838a3ea4b4bcbfe85a0c06909eead4a8cca721947cb`  
		Last Modified: Wed, 11 Mar 2026 18:34:30 GMT  
		Size: 187.1 MB (187088807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef045416bcb833198e32d8e5e952d5f2a1ea20ec079c161a2247511e34a7083`  
		Last Modified: Fri, 20 Mar 2026 17:27:34 GMT  
		Size: 85.5 MB (85545592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebafe28371f06eaee28c7daa03b00e39d14b0f2d9437eb19446f2bfebcba44e`  
		Last Modified: Fri, 20 Mar 2026 17:27:30 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99e20d4ce2c3bf4e25cebc20e5c0adf85768fc213f38e5ce26f55299ee07a2a`  
		Last Modified: Fri, 20 Mar 2026 17:27:35 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b269c3ad16bdc7266e2173a63746ff39daa31f89b45fb9e1f51eba74c5cf892c`  
		Last Modified: Fri, 20 Mar 2026 17:27:30 GMT  
		Size: 29.3 KB (29331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:cdce4bd97a1f952f7b34b1c70b13fd84c9f6733243e87c6740f6f65663a752af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f3146ad90fb1e3ec2ed3ae49ec7d5343c0c9be9a9cb241c875e60ecc1d8ca8`

```dockerfile
```

-	Layers:
	-	`sha256:8dc7826154bbb439c0110db440417c473d0684c91e5bdbf622e09d3d183db6b8`  
		Last Modified: Fri, 20 Mar 2026 17:27:31 GMT  
		Size: 11.3 MB (11342406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78151b9a96f04cd82bb31574117daab3b493c55a658dda0866c4315d24e510a9`  
		Last Modified: Fri, 20 Mar 2026 17:27:31 GMT  
		Size: 26.8 KB (26770 bytes)  
		MIME: application/vnd.in-toto+json
