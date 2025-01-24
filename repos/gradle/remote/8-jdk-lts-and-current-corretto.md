## `gradle:8-jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:f4285e50173bc080c5ec09ae61070393577118d9c853faef6d53037b1501e765
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:efa1bdda72269e2231eae2013f885c7f282fc280ba1c22ba9b7e472b7f9a4006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.7 MB (593666724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c728eaf48810429a7c46a246fc6452a921d00f836067d371a08332980e06477a`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 15:45:23 GMT
ARG version=21.0.6.7-1
# Tue, 21 Jan 2025 15:45:23 GMT
ARG package_version=1
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["gradle"]
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Jan 2025 15:45:23 GMT
WORKDIR /home/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_VERSION=8.12
# Tue, 21 Jan 2025 15:45:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54526538d126c7e701e5bad2a88c117277eaf596cbbd1417cf06d8163fba3823`  
		Last Modified: Thu, 23 Jan 2025 23:08:21 GMT  
		Size: 169.8 MB (169756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dcd16f6584988d0b5cdfb1665784e8f0b5d36d6bb3cb305d8385a89e39c590`  
		Last Modified: Fri, 24 Jan 2025 00:08:38 GMT  
		Size: 163.5 MB (163481842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facb150cd3202cb8967700de910f4720f88f24ebec1aba3f3e3a0157b1838306`  
		Last Modified: Fri, 24 Jan 2025 00:08:36 GMT  
		Size: 70.7 MB (70662728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e599a056ad35a95e0d0a0a7104c03045f71afeb0ff63d951a0a8ef0c92c2f7fc`  
		Last Modified: Fri, 24 Jan 2025 00:08:36 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c425b1d26a6ffed6554e97a62430f82cac9ff48214de30fc6eddcfdbcc635162`  
		Last Modified: Fri, 24 Jan 2025 00:08:38 GMT  
		Size: 136.6 MB (136611717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7aed9dfb09c90952dd0c4d119f3e77a7a9cb2f833ace04e6e8d1746058dec5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358e173a191555d0e130f6065bd4296bbf060fb7e02fde24b5c509a83b792838`

```dockerfile
```

-	Layers:
	-	`sha256:8911a0539d863d1098f1793ff9cddd20fc8a027b52fce367dc9377b95201a9ae`  
		Last Modified: Fri, 24 Jan 2025 00:08:36 GMT  
		Size: 10.9 MB (10880293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192e5bc3a7f9564732b1f2b60ece7f7d6d4a4d5e8135bc7c2f84b2259265e303`  
		Last Modified: Fri, 24 Jan 2025 00:08:35 GMT  
		Size: 25.6 KB (25634 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6247d09ef17c9edbfb05381d7593a6bcd475b9ded1c7c8bd041b65aeb165911f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.9 MB (588890783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a55d8d6e37f67e505db48310a95e81f24e3c2bcbf960b68f870f7e653e1603`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 15:45:23 GMT
ARG version=21.0.6.7-1
# Tue, 21 Jan 2025 15:45:23 GMT
ARG package_version=1
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["gradle"]
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Jan 2025 15:45:23 GMT
WORKDIR /home/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_VERSION=8.12
# Tue, 21 Jan 2025 15:45:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23e56705959971e6a5303bbeaaff3bb398605ff3561b9a2abe5a5f86bd115b8`  
		Last Modified: Thu, 23 Jan 2025 23:23:38 GMT  
		Size: 168.1 MB (168064367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf59a071b26184f4a6ee3dcb2183cef73bf7f896e240f5a49e121b14131c6bbc`  
		Last Modified: Fri, 24 Jan 2025 00:14:43 GMT  
		Size: 161.6 MB (161571385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a19819b9f30c810f614edcf7e1c96d19507fbfd59477d52cd82419ca06f009`  
		Last Modified: Fri, 24 Jan 2025 00:14:41 GMT  
		Size: 70.4 MB (70361603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983935a11b734d6be003ea0a39cb7819448837dbd9def2a3b4932b125a64a64a`  
		Last Modified: Fri, 24 Jan 2025 00:14:39 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affe9506619340f2228e149b1340d1f4b56fee295f8065c4f0404168ba00539c`  
		Last Modified: Fri, 24 Jan 2025 00:14:43 GMT  
		Size: 136.6 MB (136621438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a2ac933571a6fadc387426c610d8bd31e7a4b39e637f7e83a44986cded1eb476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10904054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f93c9f5eb7f06cbad698ad8ad7564957c88b3d487f04083f76a8ac65383a18`

```dockerfile
```

-	Layers:
	-	`sha256:86e35b71d01d426e8240f51076806f9594d908ebe744fc5a4590157929302569`  
		Last Modified: Fri, 24 Jan 2025 00:14:39 GMT  
		Size: 10.9 MB (10878114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc13fc48a1d79168a5543c79715229add1607233a2df0c57e5185b761ca19b23`  
		Last Modified: Fri, 24 Jan 2025 00:14:39 GMT  
		Size: 25.9 KB (25940 bytes)  
		MIME: application/vnd.in-toto+json
