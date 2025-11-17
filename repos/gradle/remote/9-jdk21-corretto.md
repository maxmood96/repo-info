## `gradle:9-jdk21-corretto`

```console
$ docker pull gradle@sha256:60e994d3f0a5c4edfbdca013413146f050a9c859d10541a966278aaf17fa0a26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:22535026484b43824ed9744a0079d05b05eeddbe15f28a5791010d7effe7f5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.8 MB (445778929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a96285fabe31918bc4bf4743a02bc5dfbf60d38d071c286a1683bdee6bb519e`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:01 GMT
ARG version=21.0.9.11-1
# Fri, 14 Nov 2025 02:17:01 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:17:01 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:17:01 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 17 Nov 2025 19:59:18 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:59:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:59:18 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 19:59:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:59:19 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:59:19 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:59:19 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:59:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:59:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:59:21 GMT
USER gradle
# Mon, 17 Nov 2025 19:59:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:59:21 GMT
USER root
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea90e0b86912d07adb758db1884d17f649cd6e3ce55ec3eff308135c598e2d`  
		Last Modified: Fri, 14 Nov 2025 03:12:58 GMT  
		Size: 170.2 MB (170193178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82416647d8cb78d22e2985b38f4fa3eb428e360097e96dc2aedfa9e0f00cbc2`  
		Last Modified: Mon, 17 Nov 2025 20:00:09 GMT  
		Size: 86.0 MB (86030490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3d76a52e6734667348d1d4c08055802e1371018eda5551adb8490e1c6a2be2`  
		Last Modified: Mon, 17 Nov 2025 19:59:58 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a8be8427a5590748efc314ec10ce15d4fd822f506095a5b8e7aae993ca7b94`  
		Last Modified: Mon, 17 Nov 2025 21:26:18 GMT  
		Size: 135.5 MB (135521965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e00b1a3324962c3cc57139f3158643ce89d763b642abaa4d466415f223d6c6b`  
		Last Modified: Mon, 17 Nov 2025 19:59:58 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7eaead409bfb331c9ce05b4931b522b30934457926057eee629dba2e8e2b0c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270242e93a758bd869c3e8bafa2e3f73d250107baadc76017cf85a3d1c111693`

```dockerfile
```

-	Layers:
	-	`sha256:3812654b77ade3ec2f484b39d77b37d1964e9a3060f8d0e684e002b539f6ac4a`  
		Last Modified: Mon, 17 Nov 2025 21:24:52 GMT  
		Size: 11.3 MB (11337144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b290203a55f23c37cdece9716b0ec1b554169e8104f27d9d22ab5efa62d39351`  
		Last Modified: Mon, 17 Nov 2025 21:24:53 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9f7603f2b0b9e8d10e0e021bc73a01e1f8deca52fece6cb085a117af0cee122b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.4 MB (442445727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb139d108b871cddb2dc905673fcd773abb956ebc811b8ed7a59dd53198df6d3`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:19:58 GMT
ARG version=21.0.9.11-1
# Fri, 14 Nov 2025 02:19:58 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:19:58 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:19:58 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:19:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 17 Nov 2025 19:59:11 GMT
CMD ["gradle"]
# Mon, 17 Nov 2025 19:59:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 17 Nov 2025 19:59:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 17 Nov 2025 19:59:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 17 Nov 2025 19:59:12 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 17 Nov 2025 19:59:12 GMT
WORKDIR /home/gradle
# Mon, 17 Nov 2025 19:59:12 GMT
ENV GRADLE_VERSION=9.2.1
# Mon, 17 Nov 2025 19:59:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Mon, 17 Nov 2025 19:59:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 17 Nov 2025 19:59:14 GMT
USER gradle
# Mon, 17 Nov 2025 19:59:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 17 Nov 2025 19:59:15 GMT
USER root
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb278807b7599e6451a57100c14ec259294cbfc0994bc81d5d0797784a723b5b`  
		Last Modified: Fri, 14 Nov 2025 03:13:39 GMT  
		Size: 168.4 MB (168449435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747cdb9a3288e8a939bc389c8703de4c1950248727de00e9cd2dbd1c35ac43d5`  
		Last Modified: Mon, 17 Nov 2025 20:00:04 GMT  
		Size: 85.5 MB (85536451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbd03f8ce0dc2527ff88d6cd9c8b6ac77aae5c634036b90f420a8567b6a4758`  
		Last Modified: Mon, 17 Nov 2025 19:59:55 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e92c4049e20221d4beea0e71f86076dc7dc0589678ca366cd22675c685a2e8`  
		Last Modified: Mon, 17 Nov 2025 22:30:34 GMT  
		Size: 135.5 MB (135521963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d440dcba8f96f15f6814f0df4c6d535bfae030965cf0b98b99992aed4e803b8b`  
		Last Modified: Mon, 17 Nov 2025 19:59:55 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3ee3de58d06f315b274cb55448a9b324674a96973894abbed05e1f249a564f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11357993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311efc400043d603b65e652492d7859ff3da2e555674a47a40475f7a0594cebc`

```dockerfile
```

-	Layers:
	-	`sha256:8c05b99c97edc5da64cba748d5588a46266039d0cb37d338472876dddff24242`  
		Last Modified: Mon, 17 Nov 2025 21:25:03 GMT  
		Size: 11.3 MB (11336146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:613168adfbe62360f82788d18bbdcd1dac7d2e0ab9fbbdcb7dac89734a7b7f55`  
		Last Modified: Mon, 17 Nov 2025 21:25:04 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json
