## `gradle:8-jdk11-corretto`

```console
$ docker pull gradle@sha256:b564b1993b7ede12cca67c53a9ac22594d83229ebec452eb0d8e0814abb2bce1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:02d802b13bb920abbc3655641931e639966c945c2aa487e9c284dda018e8e2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.4 MB (432432896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3c068df5a5251f3d58c8b0327794ebf340783c06bdee0848cc8c5d1008be5c`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:11 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:11 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:11 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 30 May 2026 02:12:41 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:12:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:12:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:12:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:12:41 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:12:41 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:12:41 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 30 May 2026 02:12:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 30 May 2026 02:12:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:12:44 GMT
USER gradle
# Sat, 30 May 2026 02:12:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 30 May 2026 02:12:44 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c301665885e6ad3943c3d90b6300031bffd77f1526c8e1fb4fcff7a8956e38`  
		Last Modified: Sat, 30 May 2026 01:11:32 GMT  
		Size: 153.5 MB (153471531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144a737cd18e53778377afc609a076805d9860cb7ab2292eb401983cfc203c7f`  
		Last Modified: Sat, 30 May 2026 02:13:15 GMT  
		Size: 86.3 MB (86265096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35596e4829d6cbb98fb056c54a0917ecb78f7dc9a9616c2e69b7957c44bad92f`  
		Last Modified: Sat, 30 May 2026 02:13:11 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d3dd2c197fad2468c779e9e1a7cc13117767de665d65ceda03e046c8682d7`  
		Last Modified: Sat, 30 May 2026 02:13:17 GMT  
		Size: 138.1 MB (138068534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c55dd46457c3d0bb3cc791459fa11bbd51e713aa132f8112bc3c7e210e8d57`  
		Last Modified: Sat, 30 May 2026 02:13:12 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:9c8573847340680a48ce4f91cfef00235a539753b5594bf9cfe2a6885f9e9f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb69b55c120c351cc2c764526652e835a6cb49233ff4db88a803a898bfb10d6`

```dockerfile
```

-	Layers:
	-	`sha256:d2c0c402165b7aec0ea6edc553ed68669bc6feb1718ce047a9120927c37e8aa5`  
		Last Modified: Sat, 30 May 2026 02:13:13 GMT  
		Size: 11.4 MB (11375665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352645d67e7606290936e8861f954accf7db1aabb583b92a030a6db940b86dce`  
		Last Modified: Sat, 30 May 2026 02:13:12 GMT  
		Size: 21.7 KB (21665 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c4cf4ee164099e5157074c4d2aad207f07a0a4298fbdf5d51f0f2d80dbb12c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.4 MB (429360364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fffc4d5da77b06b4454fc61dd1915522cca467919707177978ea1f8209a485`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:29 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:29 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 30 May 2026 02:11:59 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:11:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:11:59 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:11:59 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:11:59 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:11:59 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:11:59 GMT
ENV GRADLE_VERSION=8.14.5
# Sat, 30 May 2026 02:11:59 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Sat, 30 May 2026 02:12:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:12:02 GMT
USER gradle
# Sat, 30 May 2026 02:12:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 30 May 2026 02:12:03 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f79fb9911ea68ee16566e2d860d6457ab071bbc028d8cd54cc7be3f1495db6`  
		Last Modified: Sat, 30 May 2026 01:11:51 GMT  
		Size: 152.0 MB (152048594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09a56784dca84a65f2146be23f5d76860bfe7dfc2071831dfd97ca13739fd34`  
		Last Modified: Sat, 30 May 2026 02:12:34 GMT  
		Size: 85.7 MB (85724180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de336cba62257f95504ee53c530d173344dd02b1ad5c63d7c9555eb1d338bd51`  
		Last Modified: Sat, 30 May 2026 02:12:30 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956c61a500b462b6428989183a719a449e0cdf6fdc348a038dfafcb78d1ad907`  
		Last Modified: Sat, 30 May 2026 02:12:35 GMT  
		Size: 138.1 MB (138068534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04246842f2634422431550d7db4bef7523a2fc26332f2081a0884c2b9a46595`  
		Last Modified: Sat, 30 May 2026 02:12:30 GMT  
		Size: 59.6 KB (59551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:191e7fed8e473faab63b85d4c0f3ba2c338d266aca55f03f9c66a1938aff156b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e50c98e1c8b03a0653bebe9da525600f43d7846eab4c1a868d6e28654ef3ab`

```dockerfile
```

-	Layers:
	-	`sha256:6e9695704342c0bf84450fa980a942d5acf881e9484a5332812c57afe888f60b`  
		Last Modified: Sat, 30 May 2026 02:12:31 GMT  
		Size: 11.4 MB (11375508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76dffe44bc096719f04840adb644175780173b35baf1a64578f53ef8baaf79ed`  
		Last Modified: Sat, 30 May 2026 02:12:30 GMT  
		Size: 21.9 KB (21862 bytes)  
		MIME: application/vnd.in-toto+json
