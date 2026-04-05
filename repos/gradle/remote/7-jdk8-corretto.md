## `gradle:7-jdk8-corretto`

```console
$ docker pull gradle@sha256:f83e6ebf4cc4a10144856f00728071a244afff37d54469f3d23430e256486988
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:c6863c8bae4f6acf43886d9058fd5db0ac2dd1bd54cd2caa8e596de14f53674f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.5 MB (579477217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7792756a65221e7fdd753ead7918df8e190da43d42dfa7749293b6141334080d`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:00 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:13:00 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:00 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 03 Apr 2026 23:12:35 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:35 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:35 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:35 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:35 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 03 Apr 2026 23:12:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 03 Apr 2026 23:12:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:38 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:38 GMT
USER root
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6eaeba56796179d0d993064dbd3df43c2d205498a7f1e30808bbd70c2a9a39`  
		Last Modified: Fri, 03 Apr 2026 22:13:51 GMT  
		Size: 330.9 MB (330921554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0392c609363c40417b44d042053749007ae0089175c10b92a67074e3ff82c2`  
		Last Modified: Fri, 03 Apr 2026 23:13:20 GMT  
		Size: 65.5 MB (65458070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917dafb02183b5acedef3ae047b438804a6ab3a222f57b203d9706f224085913`  
		Last Modified: Fri, 03 Apr 2026 23:13:17 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf6e45559512b69b6c44ad9dc8e56dfe46d38885d9693da88f809e2b0a34108`  
		Last Modified: Fri, 03 Apr 2026 23:13:21 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fdae5373bf9f10febfca9ab6d615fd4d768a5498a7e41b9e1dcf01408c82fe`  
		Last Modified: Fri, 03 Apr 2026 23:13:17 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0c6016172d41607004db44f4062fef988622836f9f66c889f4ffdf97b301c0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18092908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf1095fd42e25dcdceac749d4bee002d1b18e2b0fb58b31cef41ebf82eb6a61`

```dockerfile
```

-	Layers:
	-	`sha256:d9660ba24e392b824a06dcd63b92c301a349e1dd6f4d072fcec11ff495225c77`  
		Last Modified: Fri, 03 Apr 2026 23:13:18 GMT  
		Size: 18.1 MB (18072044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6baf42eb28459303cc599f9ad8d8719f69b34f40dc3db5e73a5bbb2a878ac7a5`  
		Last Modified: Fri, 03 Apr 2026 23:13:17 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:dd6036aa7003397384e7b6816d86e2be9a9485349ac8fcab5c5675e6a8312fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385517555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93cfee554a0cb87d6a1854db379a3fbf5255e4e3914d510cb1dda40c5237140`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:10:44 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 22:10:44 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:10:44 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:10:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 03 Apr 2026 23:12:46 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:46 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:46 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:46 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:46 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 03 Apr 2026 23:12:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 03 Apr 2026 23:12:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:49 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:50 GMT
USER root
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980838d303024013ee2e8e238f5e1fd8a8322b72b587546b11a71066b190efb0`  
		Last Modified: Fri, 03 Apr 2026 22:11:08 GMT  
		Size: 118.0 MB (117961835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c9d028cd1844f46c11b19dd5db7c1a344b264bccf63c8aa7b2463abdadb3f1`  
		Last Modified: Fri, 03 Apr 2026 23:13:21 GMT  
		Size: 85.6 MB (85582271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d270f6da2b9567a42444e604e5d6c5ca05f4bbefbbc3ca82ceace2124354a8`  
		Last Modified: Fri, 03 Apr 2026 23:13:17 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989856ce696a79753dea7c5e8219e5b8410f94e9db30a095a4dc905b67db30d8`  
		Last Modified: Fri, 03 Apr 2026 23:13:22 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8387e4c1ff759fcb7ba5bc2a5cfc525f1735b813e0535f5206bf612e3094c4`  
		Last Modified: Fri, 03 Apr 2026 23:13:18 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:6c8f79fe75da11a1b0e3aaba761067ee0c08f40b976fc8f20cb5cc50ffbb3475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11657245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546e7dd75e3ccccb63f01d9e784dd9f53f0dc997872a765a15ad49e07d249e64`

```dockerfile
```

-	Layers:
	-	`sha256:ebfda7a4cc60c65275eea05e1eeba70dcf1892aec234bf16bbf3b07b0681f40f`  
		Last Modified: Fri, 03 Apr 2026 23:13:18 GMT  
		Size: 11.6 MB (11636208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce26349937bd37746358bdec09046557dbc90c1de9c286586a121a0f5d359977`  
		Last Modified: Fri, 03 Apr 2026 23:13:18 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
