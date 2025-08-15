## `gradle:jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:016f58ab502f8b164c3f87142d38d727e5d68d8818179eea71ff84a2167459b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:0a5a1932c8f9dae02e770001d5b8d3f82dea5286078ddc6b91f26cdbcffda8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.7 MB (430722818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee268e4c938fdd991aa45e3e54985bca8f0ade827df6e9db5c403e19bd7fc43`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:b9bd06b1e98f2884554d02055b944634294fa4d6f341ec4d0d7349c492676b31`  
		Last Modified: Sat, 09 Aug 2025 04:12:21 GMT  
		Size: 53.8 MB (53837959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7053c3dfee684fe542e0df754b07934a8c7d985befc94dfa121e0569a8c2f94f`  
		Last Modified: Wed, 13 Aug 2025 23:11:14 GMT  
		Size: 156.8 MB (156794651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd08758fd6b5e1e20cdb7df205d23fecfb6fd4cd87efc28897e1ea403687d1a`  
		Last Modified: Wed, 13 Aug 2025 23:13:02 GMT  
		Size: 85.6 MB (85552803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5abebf29b103383263e792268bbd6422a5ed1fd310c5036e069f65e07270dcf6`  
		Last Modified: Wed, 13 Aug 2025 23:19:52 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf7071e629101baa758b76de3ed8ce49c761bf81784cf4d733530f5a70f87d`  
		Last Modified: Thu, 14 Aug 2025 02:47:26 GMT  
		Size: 134.5 MB (134480831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821e21c7ea7a6c7dbfd8083500fd82dee3aea71a2550abaa61b34e9193cc79f0`  
		Last Modified: Wed, 13 Aug 2025 23:19:56 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:9cefd936213431652f3c88514de2b5bb5256088290c778a37e015359683bbb3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11319732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de590afd79817426dd558715430ceae5e2c5cab0aff20701a87018415ca02bda`

```dockerfile
```

-	Layers:
	-	`sha256:c0f12187590add557d9728a950d189b5e191fde1484b74fa11411c97358de20a`  
		Last Modified: Thu, 14 Aug 2025 02:24:51 GMT  
		Size: 11.3 MB (11298318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6419c2c5981865b9f8da80214907252600b56f0f4f069f121019f96b6608386`  
		Last Modified: Thu, 14 Aug 2025 02:24:52 GMT  
		Size: 21.4 KB (21414 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9178896c6cbe44a220735a4075702de3444700b3c8995c81999c629a811d413b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.9 MB (427928434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337da09dc1f10810448fdc2586343aa08ad17b688fbc9e565e0958b423b620ec`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ac9d907769c48e7b17f0e81b67567f13bdab1cc081d367ece33201a9dfaf94`  
		Last Modified: Thu, 14 Aug 2025 09:48:41 GMT  
		Size: 155.6 MB (155582881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c12dd44c28b5d21fbc6703e01f515dea0095956d6ae6fc19b03052f7daa22c`  
		Last Modified: Thu, 14 Aug 2025 18:33:55 GMT  
		Size: 85.1 MB (85077116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a752d92b62186f3f6e7c2e37b37eb90b8a9e77f1ec215d496893b32d393d80`  
		Last Modified: Thu, 14 Aug 2025 12:08:17 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6de49166dfede34ed6ad94dc76405f90d5f4bcec9acd1c183d7823dd6044c8`  
		Last Modified: Fri, 15 Aug 2025 05:24:48 GMT  
		Size: 134.5 MB (134480841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d6c3a79b969dc469b20ce6680fada5e7b42d14d8763cc09e6e9fabcfe5a10e`  
		Last Modified: Thu, 14 Aug 2025 12:11:39 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:56c1f2fdcae7121a500f7d557e8a1d468a66cf4c618e8ab1b6a83b8611fdb58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11318928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df843cfb67e7e29ffde4ac2abb9853358b5432b39c359259f2b5b4a28fd782f`

```dockerfile
```

-	Layers:
	-	`sha256:d1158c1e215e5cdbe774293c6612cae9eb1af960147cfcb7001feb57cac9e131`  
		Last Modified: Thu, 14 Aug 2025 14:24:56 GMT  
		Size: 11.3 MB (11297317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2c7413415e60ad38a11f3f202f9dd97476e4d76c68684d6d9da8342c490428`  
		Last Modified: Thu, 14 Aug 2025 14:24:57 GMT  
		Size: 21.6 KB (21611 bytes)  
		MIME: application/vnd.in-toto+json
