## `gradle:jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:5437c793e6e0758826c4b8ae9720f2a72655222d0ccb28957129242cd3dd5a23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:986ace8f5156a55c92c33f63098879143507b606bdf97aac32359e7c18c0b612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.7 MB (448698626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd6dddd7a976972df8cad325ccd0a3d7d079003523c439735d757e0c51be558`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:54 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 22:14:54 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:54 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:54 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 23:11:36 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:11:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:11:36 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:11:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:11:37 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:11:37 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:11:37 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 03 Apr 2026 23:11:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 03 Apr 2026 23:11:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:11:39 GMT
USER gradle
# Fri, 03 Apr 2026 23:11:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 03 Apr 2026 23:11:40 GMT
USER root
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a008dca2fff34c89bb6e272e0474289359dfc4286d48d849d77b48a8f3db335`  
		Last Modified: Fri, 03 Apr 2026 22:15:19 GMT  
		Size: 170.2 MB (170194101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2531baaac3993e2cdc4bf628bc0768d242792216989c339db9e4d62ae958947`  
		Last Modified: Fri, 03 Apr 2026 23:12:08 GMT  
		Size: 86.1 MB (86097597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88edae0d3f3f30add1ae1cde7065ca934ba4069a67364238b64bb860f17a7e8a`  
		Last Modified: Fri, 03 Apr 2026 23:12:04 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1069a68d44329f17e4ec35edf3b410a28101f7e17a789b1a226557cd5da42a91`  
		Last Modified: Fri, 03 Apr 2026 23:12:09 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45770b54d2cf367bc07d0b6be29e37c14b59b2b376e44d646868cfa0eb9da797`  
		Last Modified: Fri, 03 Apr 2026 23:12:04 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:8e269fc4ce6cb18968368fe8ec4ff4a8416945d651d5afde9b42fe1539ede151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9e403bd872775e3326fc71e2ecb5f3f62f92d068112e0c85666a51ba654841`

```dockerfile
```

-	Layers:
	-	`sha256:1c01f2e47b8b6d83fe101c7c2c02ce386658a9dd4beed39ce717f5303fe9a040`  
		Last Modified: Fri, 03 Apr 2026 23:12:05 GMT  
		Size: 11.3 MB (11336847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a5fd30eab339155362fe374189fb00af2ef50da55b1d802a414536bbae55409`  
		Last Modified: Fri, 03 Apr 2026 23:12:04 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a432561d6ce522747b62af3da6595223303eea230e5f19ccf3174c4a53d5547a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.4 MB (445352029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9bb52fc3932c45bd80ccc775cbb12c16a0281a3b18adcac9fcdcbafde1737ad`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:35 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 22:14:35 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:35 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:35 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 23:12:06 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:06 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:06 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:06 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 03 Apr 2026 23:12:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 03 Apr 2026 23:12:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:09 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 03 Apr 2026 23:12:09 GMT
USER root
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824d686cb23798401ffbb52de63d20a70fbef48284b9657cc9ff1b95e54649`  
		Last Modified: Fri, 03 Apr 2026 22:15:00 GMT  
		Size: 168.5 MB (168467232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c81caf859819f65e88e50fb131a365ee1b7b905676093ac60b562dc235c38c0`  
		Last Modified: Fri, 03 Apr 2026 23:12:43 GMT  
		Size: 85.6 MB (85602622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9de7300846a3b08f312b49cd81bc42ee2470d910191be0109d3000c370bd82`  
		Last Modified: Fri, 03 Apr 2026 23:12:37 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648414e7a6986d3f47ce06b70969918fb33e8dcb29f4a7369899301c2677991a`  
		Last Modified: Fri, 03 Apr 2026 23:12:42 GMT  
		Size: 137.8 MB (137808334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154dbabbb8f815c3f87c5a8df92bc46994bb5304a78edef476aff3b17fbad342`  
		Last Modified: Fri, 03 Apr 2026 23:12:37 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:bcf866541c57174171021c88831ed4b687d6de2880b9751a617efc610fdc2c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11357697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a15eda1ef7cec631607f7571f805950504584ad7822af1db9781245a7b1984`

```dockerfile
```

-	Layers:
	-	`sha256:794e71205788ae55c546956caa54a6de31000442316d162d1a77fd977034fdcc`  
		Last Modified: Fri, 03 Apr 2026 23:12:38 GMT  
		Size: 11.3 MB (11335849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd690beda5f55a857265d34d447ac2941d2471badd088dfafff038aeec2e56a`  
		Last Modified: Fri, 03 Apr 2026 23:12:37 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
