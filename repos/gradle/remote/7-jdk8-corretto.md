## `gradle:7-jdk8-corretto`

```console
$ docker pull gradle@sha256:948aae073501466ee9b9963e8e670e706ac95c08e027106afd5322434a72c4c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:cc2039745850a380f450f0af80674c8473eea7c7993615e849e25f2002b65bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **559.2 MB (559185511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3110a8475e876efdbe05c067239dba2cfb0ba99a3b3d16a4972cb15922fd5d`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ARG version=1.8.0_452.b09-2
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:1c3112c87ab2d6209030c22629180b5d1958fca3765b3cbcfbc9bcfa1ee6e425`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 53.9 MB (53880920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033c9027b1e940d2e0dc9ae5a1e6e492a721123eb0a80d6931187565809fa7cb`  
		Last Modified: Thu, 08 May 2025 17:23:21 GMT  
		Size: 330.7 MB (330690837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f80677ac89abc50397d2dbe9c07e1f0d2a83d6d60736f15c35c9fafd8f3d28d`  
		Last Modified: Fri, 09 May 2025 06:21:42 GMT  
		Size: 51.8 MB (51826347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e654402abcb99d2445ce00ca20becdc7be77d8f09e0c9c8ef9c2bd596a62a2`  
		Last Modified: Fri, 09 May 2025 06:21:35 GMT  
		Size: 1.9 KB (1939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3bd7263756d5c5374a98e3bb6ebc4af23361212e170ac4221cf12bd9ec24e62`  
		Last Modified: Fri, 09 May 2025 06:21:45 GMT  
		Size: 122.7 MB (122730537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc1cbcba8602fd7eee0b57a79f8c9341af8b8cc05ba13f1b739ea86047b18a7`  
		Last Modified: Fri, 09 May 2025 06:21:37 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a6e5a696d2e3ca0677fb20f27c925b1a66af957aac65fb82da2ffece6cbaf48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17478626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710c4d1618a6f564973a3ed7f456bb8dcf7743b52d97bad97a5eafe49c0dbd01`

```dockerfile
```

-	Layers:
	-	`sha256:5b94459b39d84c6307218cc02c713c898cfc1f31e4e71784d987897b912f71bb`  
		Last Modified: Mon, 05 May 2025 18:10:36 GMT  
		Size: 17.5 MB (17459377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09d70aa71980e6ef1a4b240856cbe74089e4a2e3616594b5e7ca2731ba3a774`  
		Last Modified: Mon, 05 May 2025 18:10:35 GMT  
		Size: 19.2 KB (19249 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:958e9cfe4ac62f6bc72fa0e5ba8a7a30b12bbe3790a87f61e730d98c74c9b5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365474711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4226c65aa920ea523ee6850ac0f0dc50d19046cb1f456d35e354c9d09f42be6f`
-	Default Command: `["gradle"]`

```dockerfile
# Sun, 30 Mar 2025 18:23:11 GMT
COPY /rootfs/ / # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["/bin/bash"]
# Sun, 30 Mar 2025 18:23:11 GMT
ARG version=1.8.0_452.b09-2
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
ENV LANG=C.UTF-8
# Sun, 30 Mar 2025 18:23:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:5804bd91a568b15c202af6e01f57d869865af0d532f8773d8faefb503ef0bbfe`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 52.8 MB (52811047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c27b9d8efe58bdddebf1270d6336fb8558fc448ba331aa18447c9af1c2c525`  
		Last Modified: Fri, 09 May 2025 00:01:34 GMT  
		Size: 117.9 MB (117857037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244bbf6d8398db5f5b280842edd44d7c6ce6202bd314e606c559f52bfabe1cc2`  
		Last Modified: Fri, 09 May 2025 10:36:46 GMT  
		Size: 72.0 MB (72014891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b3f1683efa70099eee88cf7df4559dd6982ef1e98f68d668c115607b65e017`  
		Last Modified: Fri, 09 May 2025 05:53:58 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654c58b8f23d9dddaf7fa1c0b9e985321f3c3c26185c88ee9e3b16256b157adf`  
		Last Modified: Fri, 09 May 2025 10:47:01 GMT  
		Size: 122.7 MB (122730530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417513b52872f89f08318ee741773232a2328d042694275de4b8483f522aae34`  
		Last Modified: Fri, 09 May 2025 10:47:01 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3a58a26128abdee0a5af7fbdc6754f00a1aeb08b09caed2c2c0af01ff268b8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11054592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e51eacbafd68a73fbef2e30118b8ddcc490a03c368b76fa4d5fbf133450dfa`

```dockerfile
```

-	Layers:
	-	`sha256:36a8b93bcd66b8ab00d2763b220a86dd2d5844fa29367e4e3be32aefa54a626c`  
		Last Modified: Tue, 06 May 2025 01:11:18 GMT  
		Size: 11.0 MB (11035169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ee8242cc075f4d47c3637fdbbec667ebfc993b3b3bfaf6aaa2f25e5f97c5d42`  
		Last Modified: Tue, 06 May 2025 01:11:17 GMT  
		Size: 19.4 KB (19423 bytes)  
		MIME: application/vnd.in-toto+json
