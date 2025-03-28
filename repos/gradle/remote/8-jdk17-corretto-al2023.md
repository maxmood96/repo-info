## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:401802f5d188abc13782439eb1f9058590bf70446ab3d8993f973cc74e224fe0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:675b31c2c4e03f4afccc28a91d90bb4988a6edf91f4869858e4eed8eeabaf664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.0 MB (418958895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a23efa73b9c9ddcc39291d9784254ccba99016a607a4ca306f96e5377576f16`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:27 GMT
COPY /rootfs/ / # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:27 GMT
ARG version=17.0.14.7-1
# Tue, 04 Mar 2025 19:20:27 GMT
ARG package_version=1
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a4d528c2211dd327750bd80d5d52d73eaa3c6b9fceb5c47eb1f8edbabc09fa`  
		Last Modified: Thu, 27 Mar 2025 23:58:45 GMT  
		Size: 156.5 MB (156531220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35034c17bb6619b47ac922300f5984e6838a53a9c93952d75effef4e5e9eecfc`  
		Last Modified: Fri, 28 Mar 2025 00:08:43 GMT  
		Size: 72.3 MB (72259633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94884377e658db4f50b2f28f1b3c604c209f28b0db4d5c3389fdebb3f50c5de7`  
		Last Modified: Fri, 28 Mar 2025 00:08:41 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ddfe046b8ae9d5aebfdc1a44865c72a9b011df76178c463315d46d1923af9a`  
		Last Modified: Fri, 28 Mar 2025 00:08:44 GMT  
		Size: 137.0 MB (136988179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac83e527a44513f00e00f81856c6cf84bb81c657a78536d47a18fa2493d394b4`  
		Last Modified: Fri, 28 Mar 2025 00:08:41 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:4900188d2a484b3572e408ecc5438bc2b99138af59cc8577c0570cd760754321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10760182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db8e335c99f506c63ce410cbb8ce34bb4fba07c41e91c50cceea0fbe95c8ae0`

```dockerfile
```

-	Layers:
	-	`sha256:ecb67a8fed03f94e0e8e00949892134ff0b731a0a305116f35f5849cd15decf4`  
		Last Modified: Fri, 28 Mar 2025 00:08:41 GMT  
		Size: 10.7 MB (10740436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044c295cb3ae4f1e1a32b6402779ec10061d4de1a2d631cfdc956df8802f03dc`  
		Last Modified: Fri, 28 Mar 2025 00:08:41 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e2dcea8563587a4d2cabbce9d5c2a1ce8116ef2ffc429739fcc8caa5608f3fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.6 MB (416613143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fdcf3f78fdfbd549725088ffc3800e9928acb8ea3fe71d68e718c93c6fbb1fd`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:27 GMT
COPY /rootfs/ / # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:27 GMT
ARG version=17.0.14.7-1
# Tue, 04 Mar 2025 19:20:27 GMT
ARG package_version=1
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER gradle
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
USER root
```

-	Layers:
	-	`sha256:92a376874570d50aaa72a4435a5b15fdfcdc3099600b45751b2c0705bd2c65f2`  
		Last Modified: Thu, 27 Mar 2025 02:43:04 GMT  
		Size: 52.2 MB (52247990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c8e78e2c4ad7fa3ee697afbc2c4d1adaf82b8293efdd52c99f86ce87a59b65`  
		Last Modified: Fri, 28 Mar 2025 00:14:23 GMT  
		Size: 155.4 MB (155382455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3914097e2ad0993cdd7bf0d0d1d6398b84b8976baca68cb73174a103f2d6cf58`  
		Last Modified: Fri, 28 Mar 2025 01:15:13 GMT  
		Size: 71.9 MB (71933319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5210d0406dfd7b8b5c9d2d6e6dc0eee34bc4e401604f8f71b936416d54245e`  
		Last Modified: Fri, 28 Mar 2025 01:15:10 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69daeb6c675a04e142c8376e0118d35867334e637abab0e76975c9ca8874f143`  
		Last Modified: Fri, 28 Mar 2025 01:15:16 GMT  
		Size: 137.0 MB (136988177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eb8bff90349d76b19cc22c335a3064e9398c35ea774e18ece80a7c01167786`  
		Last Modified: Fri, 28 Mar 2025 01:15:11 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:4fa18c3b11512871efc6dd77566c24195578362fc5801bf7b8e15fc5852bee17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10759379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58493c1a791e9d537975aeb4b689a63aa59b96ff709f8913d493c562243751cd`

```dockerfile
```

-	Layers:
	-	`sha256:19c9fbe9661ef3524baa7d75418127b665a1a3f70a2e7fdf5ddb7bc45ef0573b`  
		Last Modified: Fri, 28 Mar 2025 01:15:11 GMT  
		Size: 10.7 MB (10739435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6bda779fc2382a3ed8c69974ffd01eedf77a55273faea7218e3a6ae3a988125`  
		Last Modified: Fri, 28 Mar 2025 01:15:10 GMT  
		Size: 19.9 KB (19944 bytes)  
		MIME: application/vnd.in-toto+json
