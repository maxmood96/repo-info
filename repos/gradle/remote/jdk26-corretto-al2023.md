## `gradle:jdk26-corretto-al2023`

```console
$ docker pull gradle@sha256:9a3b6a100aff5bc72c58ce54ffdcc56258626a5ea8d87c875609823c48a79054
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk26-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:e8b585b255f239c78a184b6987ac6e66d6c70871e4e3bab03e453d9332fa0a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **472.0 MB (471964795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffcb74795849f6f03b0ba31934305d095ce5a0e4f70dcbc958ae2bd58d544c67`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:49 GMT
ARG version=26.0.1.8-1
# Wed, 22 Apr 2026 21:35:49 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:49 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:49 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Wed, 22 Apr 2026 22:11:43 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:11:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:11:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:11:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:11:43 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:11:43 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:11:43 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 22 Apr 2026 22:11:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 22 Apr 2026 22:11:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:11:46 GMT
USER gradle
# Wed, 22 Apr 2026 22:11:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 22 Apr 2026 22:11:46 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50190bedbe208ff9c73ab88615578d9dd88a57f1fce3e341b58ee03c54b9ba5f`  
		Last Modified: Wed, 22 Apr 2026 21:36:15 GMT  
		Size: 193.5 MB (193453798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a878235b09bb6744230a5ad662f3e91ac3b8b4edddede1ea5511df3ba7293cb`  
		Last Modified: Wed, 22 Apr 2026 22:12:18 GMT  
		Size: 86.1 MB (86104127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d6114de8426ca63988b3cb4f9903f8708fcef47ded9a23afffae918a2d2a4`  
		Last Modified: Wed, 22 Apr 2026 22:12:15 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e255710255e5fddfc75521b65c0fe475e5799e7a34f1082dc9aaa25e43de09dd`  
		Last Modified: Wed, 22 Apr 2026 22:12:20 GMT  
		Size: 137.8 MB (137808330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac100ea1e6930176383808ce1a07562645fbb2f7d2e68c69edac969e57185965`  
		Last Modified: Wed, 22 Apr 2026 22:12:15 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b29db2e8973024af3f9588827bbff2daba027d58baee887ec3034281c150b4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11366787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b694ae8a9e64074da9406f20d5638c937f26192169251b819aedac60de3ce30`

```dockerfile
```

-	Layers:
	-	`sha256:cd556fdd9326861270a4a1a4a6e8762b166cd42fbe27484d821566a8f3861d88`  
		Last Modified: Wed, 22 Apr 2026 22:12:15 GMT  
		Size: 11.3 MB (11345136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:212790b1ca97ec377b6ae964372b7a8f5a3f962bc7d07cb0de2d2de20de9e9db`  
		Last Modified: Wed, 22 Apr 2026 22:12:15 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:901fca0b863bc96886d76985a074d6460119f043e4aefaad08f8f29a6402a3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.2 MB (468157356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ed1fc75c056d554a8d918a8a4c31a8246dbcea831378d3707a6bec47049985`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:54 GMT
ARG version=26.0.1.8-1
# Wed, 22 Apr 2026 21:35:54 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:54 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:54 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Wed, 22 Apr 2026 22:11:44 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:11:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:11:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:11:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:11:44 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:11:44 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:11:44 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 22 Apr 2026 22:11:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 22 Apr 2026 22:11:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:11:47 GMT
USER gradle
# Wed, 22 Apr 2026 22:11:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 22 Apr 2026 22:11:48 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b982db98e319215a22d43ac4c3376f253018862c7a03fc6968dcd6aed6d5613`  
		Last Modified: Wed, 22 Apr 2026 21:36:19 GMT  
		Size: 191.3 MB (191274962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b76f7a073d3c69b1702dc77eed2930500570541fcd0d9d2d0b7df83a67cde0`  
		Last Modified: Wed, 22 Apr 2026 22:12:20 GMT  
		Size: 85.6 MB (85600296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a48022e5a282a2ed4ebeaa40560acf7d4323f2b60108466e450f902efb9feaa`  
		Last Modified: Wed, 22 Apr 2026 22:12:16 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7621fe54118da950986dec2a236ffadafdfd28ccc87c97ce7ccd32e4fe6629`  
		Last Modified: Wed, 22 Apr 2026 22:12:21 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a76da26b73d74468fe10aec579248ec7e10bbaa15007605df2a8de917b19416`  
		Last Modified: Wed, 22 Apr 2026 22:12:16 GMT  
		Size: 29.3 KB (29347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:ab50eb18e1de5d96de19d168c1b65c90dd139d69989c1410808d9da625bd5707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11365993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3e901a97508c091ac648f334e21f5ccf1c7a521d02073e7e0a0c4397423e95`

```dockerfile
```

-	Layers:
	-	`sha256:8b36ca1ec11406abcfe9c92397d9b2e84d832a5d71103c4c8d2d5d910f7b111b`  
		Last Modified: Wed, 22 Apr 2026 22:12:17 GMT  
		Size: 11.3 MB (11344145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9724b8d64ab5e17df25eaf70a426a59702e2550c04687bf979b8a99127f4207`  
		Last Modified: Wed, 22 Apr 2026 22:12:16 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
