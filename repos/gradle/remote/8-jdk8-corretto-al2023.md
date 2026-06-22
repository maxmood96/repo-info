## `gradle:8-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:9f373f4e53e8c85d5009e7d2555bb435168e6ee6edf80a9105fe16c502300fc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:ca99fe36923e42e5b6af3eded524397a3a61a0e6540131d74f63eb6907b531c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.7 MB (589717975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86a5062040aa4dfbe2128ee11e46cae23e8bfa5cb6c6b0c0dd0bf27f55fdded`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:01:50 GMT
ARG version=1.8.0_492.b09-2
# Mon, 22 Jun 2026 18:01:50 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:01:50 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:01:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 22 Jun 2026 18:15:46 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:15:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:15:46 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:15:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:15:46 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:15:46 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:15:46 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 22 Jun 2026 18:15:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 22 Jun 2026 18:15:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:15:49 GMT
USER gradle
# Mon, 22 Jun 2026 18:15:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:15:49 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee3ff9ac39d97098c9ffbd818c8a5f8a3bf07b29fae81ee0f8b5dc40ffe9c8f`  
		Last Modified: Mon, 22 Jun 2026 18:02:47 GMT  
		Size: 331.4 MB (331411901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f99223dd4417f70def9250119efb44cf191dd303056aacf5b9a9bdbdc62c323`  
		Last Modified: Mon, 22 Jun 2026 18:16:30 GMT  
		Size: 65.6 MB (65606440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700431c89a1acb76e7694e93deab5bfd1159858a0bcbeacf867bf4d906d3d80e`  
		Last Modified: Mon, 22 Jun 2026 18:16:27 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdb43983ade5d462fb3b487f52788d85b112712098961bc4f5a3324e92d90e3`  
		Last Modified: Mon, 22 Jun 2026 18:16:32 GMT  
		Size: 138.1 MB (138068573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5be12de655f1144e360da3faefe3c1cb2e5563548d2fb8528b888b57b0c3ab`  
		Last Modified: Mon, 22 Jun 2026 18:16:27 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b35e665d5bf968226ecb342dbf3f7acfcc0ff6175fa6e09e8c665476210dc7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18194743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a006dceb6adade64fe6492ab29b6e8a303d9e358cee0401674d629fe0b0103f9`

```dockerfile
```

-	Layers:
	-	`sha256:f65c36d9572527bb9ac1f17abf473cb5c99b0171a272a373c5d8a07bce3d271a`  
		Last Modified: Mon, 22 Jun 2026 18:16:28 GMT  
		Size: 18.2 MB (18173089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1271ee035e5bc14007238b7ae1f415993ab63609b4d5a590214cb01c26820b9`  
		Last Modified: Mon, 22 Jun 2026 18:16:27 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7e15642d8f73bb045cb2b6cb57fa007af931ea0a45c4152d0d84bcc7e014d63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 MB (395562347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ab64d35e8baa8048cc5d14f86c278ab5496fb15849836b63a00004ee8c9216`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:13:54 GMT
ARG version=1.8.0_492.b09-2
# Mon, 22 Jun 2026 18:13:54 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:13:54 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:13:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 22 Jun 2026 18:28:40 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:28:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:28:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:28:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:28:40 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:28:40 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:28:40 GMT
ENV GRADLE_VERSION=8.14.5
# Mon, 22 Jun 2026 18:28:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Mon, 22 Jun 2026 18:28:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:28:43 GMT
USER gradle
# Mon, 22 Jun 2026 18:28:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:28:44 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f3fee1ce8a11574ff2e6abadb7f32f96af61b0246ace579641b80c14c16a6c`  
		Last Modified: Mon, 22 Jun 2026 18:14:15 GMT  
		Size: 118.0 MB (117955997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413827f68d20006d6bcdc80d7c8b031de201efff9a912ab08d513349b7998d6`  
		Last Modified: Mon, 22 Jun 2026 18:29:16 GMT  
		Size: 86.0 MB (86025920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b6d65c02758eb064b95a95205bd7e53bbca971c121631d6ed8850c39deacf0`  
		Last Modified: Mon, 22 Jun 2026 18:29:12 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97f8d8fbcd19cb3cd10a1374b6c3021fba879071b30c8ccf3f8fb484bf6653b`  
		Last Modified: Mon, 22 Jun 2026 18:29:17 GMT  
		Size: 138.1 MB (138068536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c203b8b441f12e2cf932d06bac573ab877882d2851da721d4c74120400d74b6`  
		Last Modified: Mon, 22 Jun 2026 18:29:12 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a2318c565ebc6307157265335ea5212003a931899b34854c415019807b087d8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11754714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb0ca54073bd21f4602183976c68b6e848420ccefde62f86fe9bc12ecf2c518`

```dockerfile
```

-	Layers:
	-	`sha256:75d996859502591da91251918c6ee0065e8909bac144b667a142a1f631c63bb3`  
		Last Modified: Mon, 22 Jun 2026 18:29:12 GMT  
		Size: 11.7 MB (11732863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a5b052359ff9a0dfcc955d867869ca0f76558059a8ed3807645a74c70e252d`  
		Last Modified: Mon, 22 Jun 2026 18:29:12 GMT  
		Size: 21.9 KB (21851 bytes)  
		MIME: application/vnd.in-toto+json
