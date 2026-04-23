## `gradle:9-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:43d7d84414b1a2e3b791e88d1162713e1fdc5944a7fba9b2501a1d373471c0dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:228c99a189c59faf1701bfd94a8128e520c2ec20a49aef3bc8a1e7ba4269ced5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.0 MB (448960323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417e6e99032aa95a7cebbf84adc83d95e4ef3d868a9e10de709cdc51ed579de5`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:03 GMT
ARG version=21.0.11.10-1
# Wed, 22 Apr 2026 21:35:03 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:03 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:03 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 22 Apr 2026 22:11:37 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:11:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:11:37 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:11:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:11:37 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:11:37 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:11:37 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 22 Apr 2026 22:11:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 22 Apr 2026 22:11:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:11:39 GMT
USER gradle
# Wed, 22 Apr 2026 22:11:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 22 Apr 2026 22:11:40 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d119a35ffe43b60996f6905045c0bcf0304a9eddbc278c507e99e56328ddec`  
		Last Modified: Wed, 22 Apr 2026 21:35:26 GMT  
		Size: 170.5 MB (170450009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6583293b97e5923dba7c1f427abdc14fe9336401fc0a180cafc024da0e5fe43`  
		Last Modified: Wed, 22 Apr 2026 22:12:08 GMT  
		Size: 86.1 MB (86103443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12798bc264ded893463143523203336c1409d91a8fff8d64bfa44b8050644883`  
		Last Modified: Wed, 22 Apr 2026 22:12:04 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01f405536ea6952dddcc34dda046038982406a5812930a3eb5d47d771d0ff26`  
		Last Modified: Wed, 22 Apr 2026 22:12:09 GMT  
		Size: 137.8 MB (137808330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da76bffd28cd121e3f811d7e6a55eea033099f9b1216db228ea92b19b930f7aa`  
		Last Modified: Wed, 22 Apr 2026 22:12:05 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:762c786ff621f41db460a49620cd5b920ea8c1ace7eea2738776b2a338bf8049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c987e43be193ac717dea43df51ccbed43ea87af650649930e640aa137f35626`

```dockerfile
```

-	Layers:
	-	`sha256:b63c0176561c10ea833a93ec32ff138f5523c8b58d1409bd8c61c767d32a3e50`  
		Last Modified: Wed, 22 Apr 2026 22:12:05 GMT  
		Size: 11.3 MB (11337676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f7a64efa9a10f1912a1b0e3fbfb578713931fd4a4de77224bc7978414798b5`  
		Last Modified: Wed, 22 Apr 2026 22:12:04 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6c6b5ffe26b7f6e5acdbcf1382de32c9d96c456a58029e4d412425ed2a662dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.6 MB (445608214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897cf0b8ff68855cc4900627cfa3b0f6572c4d1bc5aabbcf5424294504859ad6`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:35:02 GMT
ARG version=21.0.11.10-1
# Wed, 22 Apr 2026 21:35:02 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:35:02 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:35:02 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 22 Apr 2026 22:11:14 GMT
CMD ["gradle"]
# Wed, 22 Apr 2026 22:11:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 22 Apr 2026 22:11:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 22 Apr 2026 22:11:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 22 Apr 2026 22:11:14 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 22 Apr 2026 22:11:14 GMT
WORKDIR /home/gradle
# Wed, 22 Apr 2026 22:11:14 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 22 Apr 2026 22:11:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 22 Apr 2026 22:11:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 22 Apr 2026 22:11:17 GMT
USER gradle
# Wed, 22 Apr 2026 22:11:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 22 Apr 2026 22:11:17 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681a3cd594bb2c153de3b227a9e4871406480150e30d6c8bd8e97e354169f7de`  
		Last Modified: Wed, 22 Apr 2026 21:35:27 GMT  
		Size: 168.7 MB (168723387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7a47eabf673d672e547b44abb679eccde6e66b163d4dd07119f338861e5738`  
		Last Modified: Wed, 22 Apr 2026 22:11:50 GMT  
		Size: 85.6 MB (85602746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9967246e7c5a898cfdb6912eb7ca4a78f831a27f40bdf13e8555aa14b5cb8e7`  
		Last Modified: Wed, 22 Apr 2026 22:11:45 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240db64393127c898183cfcc713f9a2d57fbbf8cf63bdcac07d875bfe7045bfc`  
		Last Modified: Wed, 22 Apr 2026 22:11:52 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4151c57a860a2946a8cf3ec9dc7a916b3f348c2c25f33b0acca5fa73a35b6402`  
		Last Modified: Wed, 22 Apr 2026 22:11:46 GMT  
		Size: 29.3 KB (29332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:fd792381c1775bf39991864387b30ea7b39158e83298a0672605cd4564bab1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb8cbe629dd8d557e4076c8adb6a29082938cf9b590fc49288fb258cdc68e6f`

```dockerfile
```

-	Layers:
	-	`sha256:13ab82a9b5a4ae62a5c54c32c7345d307ae0efacc5287669b74d0fbb768240f3`  
		Last Modified: Wed, 22 Apr 2026 22:11:47 GMT  
		Size: 11.3 MB (11336679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f16cf6646e466c581649ec9c13a9f4a0c83f3269e13b00c623c774dddcb166`  
		Last Modified: Wed, 22 Apr 2026 22:11:45 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
