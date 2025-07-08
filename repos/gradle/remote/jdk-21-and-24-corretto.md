## `gradle:jdk-21-and-24-corretto`

```console
$ docker pull gradle@sha256:9dc02278974a90dbf72dfa5ccbd60fea9007c3fabff2edeb47c2bd81e94a61b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-24-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:fdb14d479c3a0a3f7cbb5b755c92d51697e6eb5991aa5c88b2e3d95a8254a415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.6 MB (617590093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770ed986f8ee4c453e5a64a15a47c9712dfe4086935f1566439527397641defb`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 05 Jul 2025 02:23:10 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 05 Jul 2025 02:23:10 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e06cf8cec6d78c485e16f2f3cfe548f69144c0a682785a573e58f4949cf818`  
		Last Modified: Fri, 04 Jul 2025 00:14:03 GMT  
		Size: 169.8 MB (169842630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6682951064032fbd49afe2f2c2209bf5e5cdaf8ba63d53b580687eb2d680523`  
		Last Modified: Mon, 07 Jul 2025 20:32:59 GMT  
		Size: 173.1 MB (173078947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed464420137478d32994bdb25464f8f547d832a93d7141d0f1dca4b0449f1698`  
		Last Modified: Mon, 07 Jul 2025 20:33:11 GMT  
		Size: 83.4 MB (83375110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d2d16c570b287e1b21ab3435efd047c8daf9544ffa77f85856e3a08dce7980`  
		Last Modified: Mon, 07 Jul 2025 20:33:04 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c470a48a86b69de8de3903133a3f4d8899f34e51f589d78e3c9e23f8bd7a40`  
		Last Modified: Mon, 07 Jul 2025 20:32:59 GMT  
		Size: 137.5 MB (137451407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b09416ba475d1ab64d332c49a2c80c79bb60ee451291dc50c1ee32f8c5db3f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11468935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7cfb76afc33f7805894c7490cc9e46e2a7a5c6781922b344774aedc960ec43c`

```dockerfile
```

-	Layers:
	-	`sha256:d56ca9b39b707b18deac2ba66c274e1e1f935867031f3f7db4be236c0e5fa03c`  
		Last Modified: Mon, 07 Jul 2025 23:23:59 GMT  
		Size: 11.4 MB (11441636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a918d67f6c0a9836ca4e2d5dc21e5bab26f9b04d8b69640f1ac156cc2b5ad433`  
		Last Modified: Mon, 07 Jul 2025 23:24:00 GMT  
		Size: 27.3 KB (27299 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-24-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:956504b06a1128bfdb3a605eb300620d7a1575c9e25788e6ea8e2acd53974a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612437347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d787a74579f429dc5dbc85f68fb5c4cfa75284678a7b6b29f1e43f9d851f65`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 05 Jul 2025 02:23:10 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 05 Jul 2025 02:23:10 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Sat, 05 Jul 2025 02:23:10 GMT
CMD ["gradle"]
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 05 Jul 2025 02:23:10 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 05 Jul 2025 02:23:10 GMT
WORKDIR /home/gradle
# Sat, 05 Jul 2025 02:23:10 GMT
ENV GRADLE_VERSION=8.14.3
# Sat, 05 Jul 2025 02:23:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Sat, 05 Jul 2025 02:23:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:0e455f237a70326021a937388393d9d7ac6f9ae1616673300f248aeb280add13`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 52.7 MB (52717557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0168d8de5548fbc686b330ce9b494d6d492c107745388b3fd7b75bd3140ea2d6`  
		Last Modified: Fri, 04 Jul 2025 04:18:09 GMT  
		Size: 168.1 MB (168143442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d027548eb45276deac95322f5711d382f92cb7c9c1b5bccb8a4e3df987eff9ef`  
		Last Modified: Fri, 04 Jul 2025 13:56:21 GMT  
		Size: 171.2 MB (171171379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a6088572e7609f1e67e2da46c608db5dd0c4ba0b710bb4240e209225a01d1`  
		Last Modified: Fri, 04 Jul 2025 13:56:43 GMT  
		Size: 82.9 MB (82946291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dde9e981f2711a5638de32b26ec16b43bc56066377e85bc7bf217e61a7ab377`  
		Last Modified: Fri, 04 Jul 2025 04:52:15 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65660a0d544928ba4f8399ee75a72bd8d65b0516924042aeffa6a42baf218b2`  
		Last Modified: Mon, 07 Jul 2025 20:51:48 GMT  
		Size: 137.5 MB (137456891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3b19826454c24fc2dd3a02ab854c92a824bc3ba9c9984bc7bac9a2339c87e30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11467697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4521570c67dad0d4110c9016236f648cad69c82754e8dd584e17734204b469f`

```dockerfile
```

-	Layers:
	-	`sha256:c2dd9ad059ec8f9d1e8a933276dea758d7c3fd59e8eed0c16ec0a729d0ae250e`  
		Last Modified: Mon, 07 Jul 2025 23:24:08 GMT  
		Size: 11.4 MB (11440094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5786e64a86ecd97434e444304b7048b7a214476264f55cb5915506f15df06a8f`  
		Last Modified: Mon, 07 Jul 2025 23:24:09 GMT  
		Size: 27.6 KB (27603 bytes)  
		MIME: application/vnd.in-toto+json
