## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:023cc7fc0c0ebdc88c3248b72cb9f3b69943a52057c6bd11467499e5bea5d986
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:76aea798974f2e6ad535c7de8aafd6dd174bb454cd5293d2f542a399685056d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.4 MB (426357489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1642d4ffa5dedc3644e79d26a17f66de3e9244d826bfe76e51142b64d3add5c`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:10 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:10 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:34:10 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:34:10 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 22 Apr 2026 22:12:19 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:12:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:12:19 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:12:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:12:20 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:12:20 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:12:20 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 22 Apr 2026 22:12:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 22 Apr 2026 22:12:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:12:22 GMT
USER gradle
# Wed, 22 Apr 2026 22:12:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 22 Apr 2026 22:12:23 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d90e2e2edb2aa41ddb1bccceaa07382b3ea269f7c64bb96c2c732d22a0e3a7`  
		Last Modified: Wed, 22 Apr 2026 21:34:33 GMT  
		Size: 157.2 MB (157159321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c87a213474b48880e9c227183799e25833438040cc4929f9bfa1ad1ff27c62`  
		Last Modified: Wed, 22 Apr 2026 22:12:53 GMT  
		Size: 86.1 MB (86100924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b93b521a62f6f4fc0242adc6f3afe3214b4952ae8c85fbf906d45379bbc044a`  
		Last Modified: Wed, 22 Apr 2026 22:12:49 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f1623d6bf5ba2a5255e8384814cb4eddde5021f1cf96b387970233b18d55a9`  
		Last Modified: Wed, 22 Apr 2026 22:12:54 GMT  
		Size: 128.5 MB (128469406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6dc3210d31a40ca586e907c87117457787db3b6b7a1b516200db813bca65ff`  
		Last Modified: Wed, 22 Apr 2026 22:12:50 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:ffdf349dc5a2c682511f6d9ef9611fd07618e327b0469f10202baede95de5b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11280199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4330734c3c094627cb652c19094d6cf746a6cbc6600a72ff06f3c6f72c1614f8`

```dockerfile
```

-	Layers:
	-	`sha256:fdc6bf4fa51c74c0b77f4b30c11dae1a80f4e36af082c1a07ec664e7ce6743a3`  
		Last Modified: Wed, 22 Apr 2026 22:12:50 GMT  
		Size: 11.3 MB (11259486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0d89439b34d86383409e0fe841daf2ab2f4318b1e90e75af9be5009e8343a3`  
		Last Modified: Wed, 22 Apr 2026 22:12:49 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d2467ef95c6fd45c4aae98d2ec76b8c5c212878919c358720bf24adb1c080061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.6 MB (423564829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585fdd955312d3d385e37a30ea1f7449a48c5447d922ae83f66437a3e8d93a38`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:12 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:12 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:34:12 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:34:12 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 22 Apr 2026 22:12:01 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:12:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:12:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:12:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:12:02 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:12:02 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:12:02 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 22 Apr 2026 22:12:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 22 Apr 2026 22:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:12:04 GMT
USER gradle
# Wed, 22 Apr 2026 22:12:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 22 Apr 2026 22:12:05 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0561ca8443bb1344561bc8f39e7693dcf5fc60e5a67bf037c5888d8dcde2943`  
		Last Modified: Wed, 22 Apr 2026 21:34:34 GMT  
		Size: 156.0 MB (155990837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a099850568cc1483756c2ac4c6e68b467ec52499453e91419f4327d63b053d`  
		Last Modified: Wed, 22 Apr 2026 22:12:36 GMT  
		Size: 85.6 MB (85600651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5910f108ac24b379c89eb7d9d918220fd34cd680263d2ffa85862fa997e5967e`  
		Last Modified: Wed, 22 Apr 2026 22:12:33 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3440052491ec94c73843ca96857ced3f5dd6efd64f9079ed3a79ee68bf6d6918`  
		Last Modified: Wed, 22 Apr 2026 22:12:37 GMT  
		Size: 128.5 MB (128469405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa20707ffdb478853d438c1b76eb4581834bb11c11f9e8ebdc13177dbb4c140a`  
		Last Modified: Wed, 22 Apr 2026 22:12:33 GMT  
		Size: 59.5 KB (59520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e85082b259a96284c12d44f8c03cc1894cbc56fd6632378a3406db4b409e8c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11279344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e400f9057ef796985d73499a7b7b20b2e35d665d7736145b5df95e529ce5bd9d`

```dockerfile
```

-	Layers:
	-	`sha256:83b010148cd2605ef0f97b756454b5079c98ae69d1e6250e3bb2eefdd8357281`  
		Last Modified: Wed, 22 Apr 2026 22:12:33 GMT  
		Size: 11.3 MB (11258458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f20f8e7d8d27a23cf1e4ff141943f8cc17a2037de94516dcfafd14946c6e3be`  
		Last Modified: Wed, 22 Apr 2026 22:12:33 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
