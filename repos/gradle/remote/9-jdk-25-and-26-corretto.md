## `gradle:9-jdk-25-and-26-corretto`

```console
$ docker pull gradle@sha256:74f69093eb0b97cdcf570d8382980a5c338cde1b8201e9f00864423455bb71fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-26-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:1c909908d87f2ec312bc56f860d4335289cee62c4e81a23da1644f52c9b02f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **650.5 MB (650505068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32be47f8ebf5894bd279f6329c29bba7b410ebe57c1a997d02d582d7e1cea8b4`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:15 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:05:15 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:15 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:15 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 29 Jun 2026 17:14:36 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 29 Jun 2026 17:14:55 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 29 Jun 2026 17:14:55 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 29 Jun 2026 17:14:55 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:14:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:14:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 29 Jun 2026 17:14:56 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:14:56 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:56 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:58 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:59 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9187d1c0652a3fc2e5587c51e615fc4dcfb4ee369050a626cc0c5f8763605ac`  
		Last Modified: Mon, 22 Jun 2026 18:05:41 GMT  
		Size: 189.4 MB (189413466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea01044644ad1c813738969c17c448a6899e8174d6dee6de77f911d66b06641`  
		Last Modified: Mon, 29 Jun 2026 17:15:36 GMT  
		Size: 179.2 MB (179247386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234264dc0c8b3d85d2f37b0b06d1f1424b5104f061007663eeecb6b1b91ccd43`  
		Last Modified: Mon, 29 Jun 2026 17:15:35 GMT  
		Size: 86.6 MB (86646632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f271290d7655febe81db39c262ecb9de717302e28bdb90bf27ec2ba3473e44`  
		Last Modified: Mon, 29 Jun 2026 17:15:30 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c0e550bbe5d56753184fd215135c7c4a922d0ed7e41d0506cac4de3baf6ee1`  
		Last Modified: Mon, 29 Jun 2026 17:15:36 GMT  
		Size: 140.6 MB (140596005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326219183f5d03ed50821cb07025674727675e47224c6ab73dfb5fa96d819a8f`  
		Last Modified: Mon, 29 Jun 2026 17:15:31 GMT  
		Size: 25.6 KB (25608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:8514e3e18240328e05193f48f3d8e91b77a9f0c14d387ea2efb13a665a35c185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11591126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfc0cfbe00009cfd51e94f080c20f7eb1002688b710eacaf08804d332ab6d3d`

```dockerfile
```

-	Layers:
	-	`sha256:25821b7d66c053fab4f94183b58a40b43c9b2414eda0d939843f9d63baf409f9`  
		Last Modified: Mon, 29 Jun 2026 17:15:30 GMT  
		Size: 11.6 MB (11561616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ae41b99d04590b22abe2f06b53a15a1cb4d1c61d512ca7208e83d1402b73ab`  
		Last Modified: Mon, 29 Jun 2026 17:15:30 GMT  
		Size: 29.5 KB (29510 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-26-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d76a83e75b44741ca6c6a249cb3c0c8a911755b4fee4d83eb5aacbd7bc586181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **644.6 MB (644562446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e6dd4a911f1c77835f6351d16db818bbae6e7017414973fb4856640a92673d`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:33 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:15:33 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:33 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 29 Jun 2026 17:14:24 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Mon, 29 Jun 2026 17:14:48 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 29 Jun 2026 17:14:48 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Mon, 29 Jun 2026 17:14:48 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:14:48 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:14:48 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:14:48 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Mon, 29 Jun 2026 17:14:48 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:14:48 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:14:48 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:14:48 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:14:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:14:51 GMT
USER gradle
# Mon, 29 Jun 2026 17:14:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:14:51 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4f1006a54abcd81b4b8010a4470cc0f1ddc33b2dd4191d1661555e3275be62`  
		Last Modified: Mon, 22 Jun 2026 18:15:59 GMT  
		Size: 187.3 MB (187328296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8d28c15a3613f6611f744c0dc6c790840e0510e8629f1b8543f8a5196d371c`  
		Last Modified: Mon, 29 Jun 2026 17:15:31 GMT  
		Size: 177.1 MB (177119300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebd367674e900fb1e9bdce652d9b89d842f12c719004060cd4dae793345767c`  
		Last Modified: Mon, 29 Jun 2026 17:15:28 GMT  
		Size: 86.0 MB (86037074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b71e462f7476f38252380379a1182607d80f3fe550a2491f8e328b15509f9c`  
		Last Modified: Mon, 29 Jun 2026 17:15:23 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcbd686cb11fb9ab53a8a2809ec51bd38aa33cf9da5c52661c97d042bf487a18`  
		Last Modified: Mon, 29 Jun 2026 17:15:30 GMT  
		Size: 140.6 MB (140595970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa175eb3917a787413d259dfc967c33a2cf5349bc94114a7afa02687ae254745`  
		Last Modified: Mon, 29 Jun 2026 17:15:25 GMT  
		Size: 29.3 KB (29329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:eeec6a83b41c4463d5a72fe6dd17f44dc8ebd291d6299d4a5865959c3ac12149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11589914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d52f0293a1bcfa39771b102c084c6547cb012427f2e0f3827a740196661353`

```dockerfile
```

-	Layers:
	-	`sha256:f6426bcae17a6b4de1e731261e6bf20082cef5bb48e8685eb44d3c304841f392`  
		Last Modified: Mon, 29 Jun 2026 17:15:24 GMT  
		Size: 11.6 MB (11560086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db777e3f3da7bb75d22f137fc63a3c7e891e5698fa5ed1eb5435efa621afe776`  
		Last Modified: Mon, 29 Jun 2026 17:15:23 GMT  
		Size: 29.8 KB (29828 bytes)  
		MIME: application/vnd.in-toto+json
