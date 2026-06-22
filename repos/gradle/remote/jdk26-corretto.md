## `gradle:jdk26-corretto`

```console
$ docker pull gradle@sha256:1b668c4e55b1709388d4b1551f3eb612392c14e016d3c8f1c91c67a94a25cc55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk26-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:b5579b8b4ed53169eb7482d1fba9b8a62cf030dfe5a814599cd302322fe1c627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **475.3 MB (475289878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca61f8957cf8bf94b47c9f8fc8b62553bb0282cf3010de4d38390ef12123968a`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:41 GMT
ARG version=26.0.1.8-1
# Mon, 22 Jun 2026 18:05:41 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:41 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:41 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 22 Jun 2026 18:15:17 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:15:17 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:15:17 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:15:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:15:17 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:15:17 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:15:17 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:15:17 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:15:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:15:20 GMT
USER gradle
# Mon, 22 Jun 2026 18:15:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:15:20 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89540e7f1948b9cdfd916831c36aadc51bc055ba3210b16a29c727cca6e3c68`  
		Last Modified: Mon, 22 Jun 2026 18:06:04 GMT  
		Size: 193.4 MB (193449808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce62af72a211cf41a4dd0cc581cdc1a73227263e3b5e58dc2a06ecf1aa0b756`  
		Last Modified: Mon, 22 Jun 2026 18:15:52 GMT  
		Size: 86.6 MB (86643487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0048e78ab2f555abab9790988b194ef401646be16122a902b5f47a1d9123797`  
		Last Modified: Mon, 22 Jun 2026 18:15:48 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52c3a233c11b792c5451de477e807db85e4b53faffef9c0fc11ba61395f2a9d`  
		Last Modified: Mon, 22 Jun 2026 18:15:53 GMT  
		Size: 140.6 MB (140595105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba2c84b76209869765c44c5bcddf42417247d2377498b75b04ca1a187f4faf6`  
		Last Modified: Mon, 22 Jun 2026 18:15:48 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7a62d843b94f4d3e703556af9126915b98df07c90a79deb8545d093ca93404f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11414169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb334b802fbf8b5a3aec57cdecb8d8ed2f3451ca412230c0e47c3a061004ebf`

```dockerfile
```

-	Layers:
	-	`sha256:aa2fb76d6ea5b2c1381c4d7054fe643ab6a13dd35fba0e182322048e54fbb181`  
		Last Modified: Mon, 22 Jun 2026 18:15:49 GMT  
		Size: 11.4 MB (11392519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e67ca7f93a1b5be147743432e065139dcf9cfd4c2513f22dd3aa8aae0deb1537`  
		Last Modified: Mon, 22 Jun 2026 18:15:48 GMT  
		Size: 21.6 KB (21650 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:67e3dcb45f873a6093f50b8318fcd05b8d1d0a740d7a9ab269850f464fc90102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.4 MB (471392278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df307a0a203b66ff547022ab110a5c249eacd78914a5dd01b672678a1f1bc9aa`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:41 GMT
ARG version=26.0.1.8-1
# Mon, 22 Jun 2026 18:15:41 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:41 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:41 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 22 Jun 2026 18:27:05 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:27:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:27:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:27:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:27:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:27:05 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:27:05 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:27:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:27:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:27:08 GMT
USER gradle
# Mon, 22 Jun 2026 18:27:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:27:08 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d96dfa1bda3810217adf300288ddcf0930ea9cdb2f132ac9d7c70180a735c41`  
		Last Modified: Mon, 22 Jun 2026 18:16:07 GMT  
		Size: 191.3 MB (191273399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f95791572a903d5457c37c88953e05188c2048022938e3f914ff5eb7e802be1`  
		Last Modified: Mon, 22 Jun 2026 18:27:41 GMT  
		Size: 86.0 MB (86042078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b45abe1506ae2c6b7e67cd608082772cb92573f982f690b43fd36b7a948397`  
		Last Modified: Mon, 22 Jun 2026 18:27:36 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c309b7e51a688b3fa8d0b530501ec80baf4cffd8e497b59ac5dfeb7bdf42ed24`  
		Last Modified: Mon, 22 Jun 2026 18:27:43 GMT  
		Size: 140.6 MB (140595104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2a8a991a76516053d0d0c29c862ae5b5714fe166af46878f82d96059e4751b`  
		Last Modified: Mon, 22 Jun 2026 18:27:37 GMT  
		Size: 29.3 KB (29331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:ba65ffd4f027047e07eacd790e25a683291124674aba47a1ca53baf9feb2e0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11413375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04e45a6f5889751239ef9214dba06d48cf41b2dc32de99fc3804a89a0d2a970`

```dockerfile
```

-	Layers:
	-	`sha256:a804ac5863e222c4665d9d36cdeb4f817cc65af45543c5b9a306156ad71e5ac3`  
		Last Modified: Mon, 22 Jun 2026 18:27:37 GMT  
		Size: 11.4 MB (11391528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6febcf19b377bd1dd04b70001c628fc219ccdb0f9e6fee0f8885f88f193c4f3c`  
		Last Modified: Mon, 22 Jun 2026 18:27:36 GMT  
		Size: 21.8 KB (21847 bytes)  
		MIME: application/vnd.in-toto+json
