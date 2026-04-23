## `gradle:9-jdk25-corretto-al2023`

```console
$ docker pull gradle@sha256:7f0ad7ab35752d19633d374fb8b6575fe6fb4f930487fa025e1c2d128dfa4dcb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:7f9f147ca5de25e86e8fba39f22bb3e3f2452d53468bc75318184fa81b353dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.9 MB (467928367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa5ea9d40743cf09958de3f24a4032073a9461afe6f14ba610fd4cf776cc934`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:13 GMT
ARG version=25.0.3.9-1
# Wed, 22 Apr 2026 21:35:13 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:13 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:13 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 22 Apr 2026 22:11:11 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:11:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:11:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:11:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:11:11 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:11:11 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:11:11 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 22 Apr 2026 22:11:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 22 Apr 2026 22:11:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:11:13 GMT
USER gradle
# Wed, 22 Apr 2026 22:11:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 22 Apr 2026 22:11:14 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2591012b75e095c7dcd4fd8cb3a454594c85ade551fce59b2251c4c9be4390a2`  
		Last Modified: Wed, 22 Apr 2026 21:35:39 GMT  
		Size: 189.4 MB (189416737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df8f4d0bff0fa17618417b3ee08bb131c67712db3bf9a7f9dbd545b84bc0611`  
		Last Modified: Wed, 22 Apr 2026 22:11:45 GMT  
		Size: 86.1 MB (86104745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1535d4fc5e5c151ae7a6f18c4908f7eb2f3ccebceb1d0256c5f4deb0b28d91b`  
		Last Modified: Wed, 22 Apr 2026 22:11:41 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f468f65d16a19c860f108ae933c2ac5a088e8986368cfc49dfa354cf01933b6c`  
		Last Modified: Wed, 22 Apr 2026 22:11:46 GMT  
		Size: 137.8 MB (137808335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7a288cb7f8e3b055518c35fb6c163b1915045716684590716eba7189bf0418`  
		Last Modified: Wed, 22 Apr 2026 22:11:42 GMT  
		Size: 25.6 KB (25618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e190f680faa05789147225f5563cbea661549f78d7fa21603b974fb6021b74b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11372114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f754b4182edbc6022a081f8bc13f18a2829622f4bc52325efb1f60d91b4d0686`

```dockerfile
```

-	Layers:
	-	`sha256:c01f82752ae0a59326cbafd55405db8c8f1281a194ab1af63dfeaaacafc72f13`  
		Last Modified: Wed, 22 Apr 2026 22:11:42 GMT  
		Size: 11.3 MB (11349845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b27d6f4601faa704e14b12dc315a394b443212fa08aa509b6aaf3924cb2d4a02`  
		Last Modified: Wed, 22 Apr 2026 22:11:41 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:46888db8aee58fa2b2a48857f4631e49a83b6c00940f1fa358ac3598e6a17d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.2 MB (464218331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b32f63a7c34ab0a9ae3a03618ae8723d7fe5be62af63f471b1266c7695f56a2`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:22 GMT
ARG version=25.0.3.9-1
# Wed, 22 Apr 2026 21:35:22 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:22 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 22 Apr 2026 22:10:45 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:10:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:10:45 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:10:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:10:45 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:10:45 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:10:45 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 22 Apr 2026 22:10:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 22 Apr 2026 22:10:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:10:48 GMT
USER gradle
# Wed, 22 Apr 2026 22:10:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 22 Apr 2026 22:10:49 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087f14a6bed93dc6cc05213cc8b33990b3e8252952c2db40348f9406226b36d2`  
		Last Modified: Wed, 22 Apr 2026 21:35:50 GMT  
		Size: 187.3 MB (187333284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d71c77449c721365739ad83980369b3a523a0b3a50e9c022d02d8a59dc6304d`  
		Last Modified: Wed, 22 Apr 2026 22:11:22 GMT  
		Size: 85.6 MB (85602962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25da0e9f91905f668df8effdd1a744dab18782460e203c645ec268d1a92c6af2`  
		Last Modified: Wed, 22 Apr 2026 22:11:17 GMT  
		Size: 1.6 KB (1642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6f0304f90bccfcb2a8a6a28fcc8327add1e59f0a774a283b1bda959d3fdff7`  
		Last Modified: Wed, 22 Apr 2026 22:11:23 GMT  
		Size: 137.8 MB (137808332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e879637da173717fbb87b3d828097b187dada84c32e63265babb1adaea2df843`  
		Last Modified: Wed, 22 Apr 2026 22:11:18 GMT  
		Size: 29.3 KB (29340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b84e4829ee9bfc918ccc75f3de522b4fcffdc5b611b03a7654c666b1d3b75f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb77ecd64507cc3a8ed93a02c5309186c257f1904022cc049e4ee0e122923e0`

```dockerfile
```

-	Layers:
	-	`sha256:37b5421067fc7b965beff89fd1a5b395224e4a2f34e87f70b35137f3ef33a2b8`  
		Last Modified: Wed, 22 Apr 2026 22:11:18 GMT  
		Size: 11.3 MB (11348883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e83f9c2ae5486e0db836100376b29f2dfd36386eb87fa06e816b6b3b4bcd06a`  
		Last Modified: Wed, 22 Apr 2026 22:11:17 GMT  
		Size: 22.5 KB (22489 bytes)  
		MIME: application/vnd.in-toto+json
