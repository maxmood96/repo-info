## `gradle:jdk25-corretto-al2023`

```console
$ docker pull gradle@sha256:60c88824b0ff5cfb03c9ddd8994a25e4139ca35f77e615829e8e620d6236ee72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk25-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:858458022778f7f5d92f02e4437c96ebb79183f3ce0eb46d5d19baac10bbaf37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.7 MB (467700053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473d01d7405cffe7a1bfc5941842adc385b56024a9fadf0cf905049eded6a5a5`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:49:36 GMT
ARG version=25.0.2.10-1
# Mon, 13 Apr 2026 22:49:36 GMT
ARG package_version=1
# Mon, 13 Apr 2026 22:49:36 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:49:36 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:49:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 13 Apr 2026 23:39:41 GMT
CMD ["gradle"]
# Mon, 13 Apr 2026 23:39:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 13 Apr 2026 23:39:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 13 Apr 2026 23:39:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 13 Apr 2026 23:39:42 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 13 Apr 2026 23:39:42 GMT
WORKDIR /home/gradle
# Mon, 13 Apr 2026 23:39:42 GMT
ENV GRADLE_VERSION=9.4.1
# Mon, 13 Apr 2026 23:39:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Mon, 13 Apr 2026 23:39:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 13 Apr 2026 23:39:44 GMT
USER gradle
# Mon, 13 Apr 2026 23:39:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 13 Apr 2026 23:39:45 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965f1a19918fd21b127f9ac8bada2cedd82d65adae53850afab82d4eff565fd`  
		Last Modified: Mon, 13 Apr 2026 22:49:58 GMT  
		Size: 189.2 MB (189188193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce11aae16ef040ad6819d4e5d8abaf0ce8293f7058116207c54f975c1a32e2d`  
		Last Modified: Mon, 13 Apr 2026 23:40:15 GMT  
		Size: 86.1 MB (86104962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003b4cef7b1fea87a1b111fdd94dc4a325668d0d9227adb68da8a16ac579093d`  
		Last Modified: Mon, 13 Apr 2026 23:40:11 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89985092ff1ea72d67a1d0c80788cb0815fbd46a930195db9844fdad550aa55c`  
		Last Modified: Mon, 13 Apr 2026 23:40:16 GMT  
		Size: 137.8 MB (137808352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ca4181ad4da36f74cc9fb5903a30c352f3b0f0755e55a0ff6c10a6c3c45901`  
		Last Modified: Mon, 13 Apr 2026 23:40:11 GMT  
		Size: 25.6 KB (25613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:11c6c5d9505df8c9921491564b4a2a958803f92fd8beae7859bc415eef4a68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93a282136ccc054441f738420739543788d11c7d313ebeb38db73aaeb0bd92a`

```dockerfile
```

-	Layers:
	-	`sha256:e7d923f48389f930e79886577f071724039a5ae0e0deb8a3034a8998895b59cc`  
		Last Modified: Mon, 13 Apr 2026 23:40:12 GMT  
		Size: 11.3 MB (11349036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc044ceb6f99179700c970b2076b55375e6a1c82081801d2832c4710af4c3ab7`  
		Last Modified: Mon, 13 Apr 2026 23:40:11 GMT  
		Size: 22.3 KB (22268 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3bf51efa1e85c13d37c0e8a4309629569252aa07f76a02269231aa61f657edc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.0 MB (463975525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed50cf55fa26a7884261ba0f2b00c0d31c3721d5c658e59440eb6405269ee23`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:12:21 GMT
ARG version=25.0.2.10-1
# Mon, 13 Apr 2026 23:12:21 GMT
ARG package_version=1
# Mon, 13 Apr 2026 23:12:21 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:12:21 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:12:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 13 Apr 2026 23:53:20 GMT
CMD ["gradle"]
# Mon, 13 Apr 2026 23:53:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 13 Apr 2026 23:53:20 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 13 Apr 2026 23:53:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 13 Apr 2026 23:53:20 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 13 Apr 2026 23:53:20 GMT
WORKDIR /home/gradle
# Mon, 13 Apr 2026 23:53:20 GMT
ENV GRADLE_VERSION=9.4.1
# Mon, 13 Apr 2026 23:53:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Mon, 13 Apr 2026 23:53:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 13 Apr 2026 23:53:23 GMT
USER gradle
# Mon, 13 Apr 2026 23:53:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 13 Apr 2026 23:53:23 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4012a6eeb902fd47c054143eafd4fb0b52ee79fd3d3e5359b5394be8cad6db3`  
		Last Modified: Mon, 13 Apr 2026 23:12:47 GMT  
		Size: 187.1 MB (187089592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce63837be55df3e507fb7f9befb4226b8516eae82af24f2df5865a26836a87fe`  
		Last Modified: Mon, 13 Apr 2026 23:53:55 GMT  
		Size: 85.6 MB (85603850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1acbc1f328fa0025d63adf4c12f5392d862d02a194f2f90de2136f912ae2bbbe`  
		Last Modified: Mon, 13 Apr 2026 23:53:52 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c014556274830ba17fe42871c41d739c78cb1fce61843e7de182b54008f26f`  
		Last Modified: Mon, 13 Apr 2026 23:53:57 GMT  
		Size: 137.8 MB (137808329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9dea779c339e0155332d1a1752f7604dd866e11ada62da4a1ca626483199d`  
		Last Modified: Mon, 13 Apr 2026 23:53:52 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:d15547914f43fd95bed39699e613a251d9398711c031f8f4fb5a619a668f6324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40271dee8daf4fdb280b3a2ef18c08cacd3351b3484eefb2657a02225c60d14`

```dockerfile
```

-	Layers:
	-	`sha256:ea6d270254de6096b5916d89c536e9b2c10c63266f931a290cc25c1fe3faec39`  
		Last Modified: Mon, 13 Apr 2026 23:53:53 GMT  
		Size: 11.3 MB (11348073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b96b3e269d433d04ec42e50b85ad062700796acfc4ad13d9f4dfd6f6c6bf023`  
		Last Modified: Mon, 13 Apr 2026 23:53:52 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
