## `gradle:jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:2b825feaecbdd9441ad66e3e3d8cf57e0eb43d020fc76ba4edf67c8d97c227d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:198572db9204366d496b62189915fa2b2193e04e084d0e5853de0da7ad3a4955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451473126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f9aea737804f582343c96b2ec2ff05ff89c3bebc24496880f46e85035c749a`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:23 GMT
ARG version=21.0.11.10-1
# Fri, 22 May 2026 21:12:23 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:23 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 22 May 2026 22:06:03 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:06:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:06:03 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:06:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:06:03 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:06:03 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:06:03 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 22 May 2026 22:06:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 22 May 2026 22:06:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:06:06 GMT
USER gradle
# Fri, 22 May 2026 22:06:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 22 May 2026 22:06:06 GMT
USER root
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff121652fd8f348860139cbe6d75ae68e9269ce4de11a62feb50538f65ba9d01`  
		Last Modified: Fri, 22 May 2026 21:12:44 GMT  
		Size: 170.4 MB (170447593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af38263da4c1d9d7e39771e8c715ccd20b4923d00b25a3829ad64368fe47825`  
		Last Modified: Fri, 22 May 2026 22:06:38 GMT  
		Size: 86.2 MB (86188853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c960238c10dfe0134569d0250213ae8c0761bdb717e3fb48bf9429c8928b6472`  
		Last Modified: Fri, 22 May 2026 22:06:33 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70864b68f792839d827c8d62aaf0da85a50ff351449bba11902f41599d1b3fc4`  
		Last Modified: Fri, 22 May 2026 22:06:38 GMT  
		Size: 140.2 MB (140236948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6642d939334994e445301e414d166852fb0ba74e24edb2b0733cc3c4e846a27`  
		Last Modified: Fri, 22 May 2026 22:06:34 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:645f7f8b16ce1e60a8487e3e50edb8c7fe140ff779efb0d82078910d8017f478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11389737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c201b525f2c9c94bf2133a5a799dd881a22e57eed035730814a53c3980ae7c9`

```dockerfile
```

-	Layers:
	-	`sha256:c873cf23c569c42efd38f0b39b892a7e574f00d6eb2101d5ef15b167721e1f3e`  
		Last Modified: Fri, 22 May 2026 22:06:34 GMT  
		Size: 11.4 MB (11368086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1290fc0e5ef3e2929aeabe3968f499102ebc627787841bad13b209896afe7940`  
		Last Modified: Fri, 22 May 2026 22:06:33 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7803eb2dbab1ba2292269d47532ae164c8f4eb9231e1d442b306f0a9498f2b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.1 MB (448135011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f436e448abaab1cb13e877fd261700f6a97919d3fc77f9eb5a26819e05fff1ae`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:07 GMT
ARG version=21.0.11.10-1
# Fri, 22 May 2026 21:12:07 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:07 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:07 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 22 May 2026 22:06:49 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:06:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:06:49 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:06:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:06:49 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:06:50 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:06:50 GMT
ENV GRADLE_VERSION=9.5.1
# Fri, 22 May 2026 22:06:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Fri, 22 May 2026 22:06:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:06:52 GMT
USER gradle
# Fri, 22 May 2026 22:06:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 22 May 2026 22:06:53 GMT
USER root
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c09cffee1deca5889479ce29d580c920fd0813f91a6e360f166fd36a236292a`  
		Last Modified: Fri, 22 May 2026 21:12:32 GMT  
		Size: 168.7 MB (168720490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2c73367e34bf19d731825d1eabb48ec3d968b0160e1dd6ccf5caa0d00890bd`  
		Last Modified: Fri, 22 May 2026 22:07:25 GMT  
		Size: 85.7 MB (85692104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d093c3b4d8339b75728324eeb8ab22924cdc25d5628308052374deac1da8dda`  
		Last Modified: Fri, 22 May 2026 22:07:21 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c46898d72e72ec82232a02adea42793993ffc3ce4b53b48ab9eca27ff3f4173`  
		Last Modified: Fri, 22 May 2026 22:07:26 GMT  
		Size: 140.2 MB (140236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff15895c103f6b597449b530105e4fe1429ea2bae16b2978ce8b6a36e476b303`  
		Last Modified: Fri, 22 May 2026 22:07:21 GMT  
		Size: 29.3 KB (29339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b2dda9f89d14212fd4b4573fb4d8492edbb0307047cc7e0ce0fc19cf71b39c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11388937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aca347c665b77d2b2f084e55348497750ed0e561a2757055d103ce1f74439f6`

```dockerfile
```

-	Layers:
	-	`sha256:9bfa8f18264e5944c21dc67c811a1c60d3ce6df441640d68b3f452e4c2cde996`  
		Last Modified: Fri, 22 May 2026 22:07:22 GMT  
		Size: 11.4 MB (11367089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17aaf08cb1607118b50e0280d65c8e8b099f2b7902052f1394eb1c3961478ac5`  
		Last Modified: Fri, 22 May 2026 22:07:21 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
