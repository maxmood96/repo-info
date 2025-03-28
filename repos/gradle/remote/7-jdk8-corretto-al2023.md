## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:5b2e1c79fbde60a758c3509db580ee0f861a9efa8419ca7d441de324cba67baf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:5e1be9b6bc938688bfe6cd3a9d485cefcf467d4fc6175a36d6cef084b2e0983c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559167158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e8c6cde3ce7fda1f0d2045819ef47cf98d07aa81302985734cce0d78f3b148`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:50 GMT
COPY /rootfs/ / # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:50 GMT
ARG version=1.8.0_442.b06-1
# Tue, 04 Mar 2025 19:20:50 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 19:20:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 04 Mar 2025 19:20:50 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:50 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:50 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:50 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 04 Mar 2025 19:20:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 04 Mar 2025 19:20:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
USER root
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30362d83c623e5aabae5bacabced60f6c1539274da394b9898f7142c70f0516`  
		Last Modified: Thu, 27 Mar 2025 23:59:29 GMT  
		Size: 331.5 MB (331481854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4310a6c299288bfc878717ca9830e44af0c9652ac161a011019212723c6231`  
		Last Modified: Fri, 28 Mar 2025 00:09:05 GMT  
		Size: 51.8 MB (51774628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a059b8282fd99863e6538372d4e5a48733e848e4cbeca74bbfab1507a9babe7`  
		Last Modified: Fri, 28 Mar 2025 00:09:02 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72dd77aef307971d88e1816c80d0920af87326d579f9b6cacd1f041a4ec9c24`  
		Last Modified: Fri, 28 Mar 2025 00:09:06 GMT  
		Size: 122.7 MB (122730501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb422047cce9ee1330b5542feaa20a51294aecd5f6039c443ab6a7a99b520ad`  
		Last Modified: Fri, 28 Mar 2025 00:09:03 GMT  
		Size: 54.9 KB (54909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:c06c8b4d1f45ef0d707a1eaaac457e5e328351d786273b9950ee25022df15a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17470686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20be5b6bc1b9c074546849f0d5adf605857e3bdb01382bd49d7004516c3cfe3a`

```dockerfile
```

-	Layers:
	-	`sha256:617f90d2f4849c074c87a52ad2945582a118c44e5e2900f3c1c129800a32e56f`  
		Last Modified: Fri, 28 Mar 2025 00:09:03 GMT  
		Size: 17.5 MB (17451436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50fbc9fb641173b539efb584e50436c5115f4ab2162a6ca5842a9e2c3fae65f3`  
		Last Modified: Fri, 28 Mar 2025 00:09:02 GMT  
		Size: 19.2 KB (19250 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:507aaf7cb579003ebde52d92fe05559ba1a49f861cbbcc66fc59eb43ba6bef52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365650394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4acf27a8f4750f4877349c8560c5231e89412f7c9137756e20a3814921ed191a`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:50 GMT
COPY /rootfs/ / # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:50 GMT
ARG version=1.8.0_442.b06-1
# Tue, 04 Mar 2025 19:20:50 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 19:20:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 04 Mar 2025 19:20:50 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:50 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:50 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:50 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 04 Mar 2025 19:20:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 04 Mar 2025 19:20:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:50 GMT
USER root
```

-	Layers:
	-	`sha256:92a376874570d50aaa72a4435a5b15fdfcdc3099600b45751b2c0705bd2c65f2`  
		Last Modified: Thu, 27 Mar 2025 02:43:04 GMT  
		Size: 52.2 MB (52247990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee0e79f59a6fe07537aa74fbc382a6783e3fa67c347c3b6bad2f131b6c51f66`  
		Last Modified: Fri, 28 Mar 2025 00:05:35 GMT  
		Size: 118.7 MB (118699430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4226cfcdfddf67cc1b2497408376861525cf3fa891f166f0410a04a7b25b4f0`  
		Last Modified: Fri, 28 Mar 2025 01:17:39 GMT  
		Size: 71.9 MB (71911231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffa7abc99e2efe421a4485bbc1316d8ec22fc8cdf1810abc0b5cf57efa53f7`  
		Last Modified: Fri, 28 Mar 2025 01:17:37 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fa0c32a2a30e72066060c6a33e53df642c1e88ba37b55a9bfa8e86a17b6be8`  
		Last Modified: Fri, 28 Mar 2025 01:22:48 GMT  
		Size: 122.7 MB (122730528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff582363bfa54286c2afc6dd48c1e2cfe78001f4dd7f7a05a5fef606800cedb8`  
		Last Modified: Fri, 28 Mar 2025 01:22:45 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:59c6fa942268fb23e91a8c5ab116c9222bfc74c059ad72e3375c8bb513298a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (11046677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f6e5cd783cfdbe0fd1a5e4a69541ab8f35b823c60a40176164e06dfdd66ffc`

```dockerfile
```

-	Layers:
	-	`sha256:8dc2946ceebaa2c3619693a022dba4d5223789978d9469741b51cb3eb51925fb`  
		Last Modified: Fri, 28 Mar 2025 01:22:45 GMT  
		Size: 11.0 MB (11027254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff1cbdcb1102b6735ad9c0d34302e7d38830beebcb633b87057cc7a0d8086d24`  
		Last Modified: Fri, 28 Mar 2025 01:22:44 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.in-toto+json
