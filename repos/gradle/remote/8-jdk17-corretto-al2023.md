## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:9a40f91169b9685e9d25c73722b7f8dea9e1e7aa43dc4fc8a1acda1614a05eca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:047039ca4cb0d3658a811f3f9b3b42f63fa8ee9f1f8d2349b226a25fcb86e646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.4 MB (434423750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c90197dae1cac8efc61ec70cc68a5c5febed8e16a16999d7adcd234e7e57310`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:24 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 18:59:24 GMT
ARG package_version=1
# Wed, 21 Jan 2026 18:59:24 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:24 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:17:15 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:17:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:17:15 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:17:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:17:15 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:17:15 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:17:15 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 21 Jan 2026 19:17:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 21 Jan 2026 19:17:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:17:18 GMT
USER gradle
# Wed, 21 Jan 2026 19:17:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 21 Jan 2026 19:17:18 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9611f4d384734b62e775c9d6504436549d04bb86a1c85fb4d696880e755c9a`  
		Last Modified: Wed, 21 Jan 2026 18:59:47 GMT  
		Size: 156.9 MB (156916086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e27479efc0ae73b56d1e4a74d4f3306059de45d52cef6f93f6e697528534d09`  
		Last Modified: Wed, 21 Jan 2026 19:17:49 GMT  
		Size: 86.0 MB (86034748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3141951710bdd8b16da646d88758ef0f382c386a21574755b486ba52aa7f34a5`  
		Last Modified: Wed, 21 Jan 2026 19:17:45 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347a50d1c64146573558ad88dec1c60aae24d3305cb477bdf1045583eec8ccdd`  
		Last Modified: Wed, 21 Jan 2026 22:05:46 GMT  
		Size: 137.4 MB (137395130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a89b8581674f179d5d5c33ccaf97763ae4f9fec187317f5fd129ddb4ccb4b34`  
		Last Modified: Wed, 21 Jan 2026 19:17:45 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:f8de5b0589cbba51fe2adba9baae106e9da32b19cd3c0b97f8d6bfb73fc002c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11360574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d32d5afd9eda045d1c02248f85b37233739857a2a297d49575bc06097b22002`

```dockerfile
```

-	Layers:
	-	`sha256:63f9fb3029e15255146b17ce97b517110e731c6591a534830ae465dbf4b26a7c`  
		Last Modified: Wed, 21 Jan 2026 21:21:38 GMT  
		Size: 11.3 MB (11339848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed05f41479334755c27bc166193d92b14b1164f5c2c28a718f9f25141d34fee9`  
		Last Modified: Wed, 21 Jan 2026 19:17:45 GMT  
		Size: 20.7 KB (20726 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2a377a73829f52edf1a7b180eb5f6f26d0e6294e59b5e51249018c05b617dc52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.6 MB (431605412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5453549c7a8886c34fdc5cee6284eb0b98b5181aab040ec52a57fbbbeb6a5a99`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:37 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:37 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:00:37 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:00:37 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:17:01 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:17:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:17:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:17:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:17:01 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:17:01 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:17:01 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 21 Jan 2026 19:17:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 21 Jan 2026 19:17:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:17:03 GMT
USER gradle
# Wed, 21 Jan 2026 19:17:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 21 Jan 2026 19:17:04 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e98527feec5a6e3b7d9dd4edae394a807158bda7cdb1fdad45eafe42104a93`  
		Last Modified: Wed, 21 Jan 2026 19:14:36 GMT  
		Size: 155.7 MB (155718940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65de7735e1520eb38553cfb6bb802d3d37c9998dd642be1d897b0ed8d14a9a8`  
		Last Modified: Wed, 21 Jan 2026 19:17:35 GMT  
		Size: 85.5 MB (85515784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a8a29a5e743cd1daca4488cfa9edd9cf45b36218fdf1120b8112cbec08521d`  
		Last Modified: Wed, 21 Jan 2026 19:17:56 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f999ae9e944393ad442d17e03417f2f929feda7187e0f51fdedc1b01772f166`  
		Last Modified: Thu, 22 Jan 2026 00:05:13 GMT  
		Size: 137.4 MB (137395129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a95bbe1e9e0783cf9bb6de5f8f06b9b7de5e0aae5bdae550565c8823dfd5b0`  
		Last Modified: Wed, 21 Jan 2026 19:17:32 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:285e186760aecb66fac0bdadd1892edea504043ccf63f8e51e360d3e979fd699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b5249f250e25b259b9e432f1f2ee2b4d28da40ffc434bb479a5619a50401fd`

```dockerfile
```

-	Layers:
	-	`sha256:2fe6eb788856a069160cbddff9360d1090b7282a50bd872ae1cad04f1ce27915`  
		Last Modified: Wed, 21 Jan 2026 21:21:18 GMT  
		Size: 11.3 MB (11338823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45890c2f71f01f011a9a9ff954522e260d90b283992328b4a8d8a1a50effec07`  
		Last Modified: Wed, 21 Jan 2026 19:17:32 GMT  
		Size: 20.9 KB (20899 bytes)  
		MIME: application/vnd.in-toto+json
