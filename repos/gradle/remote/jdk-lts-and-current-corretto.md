## `gradle:jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:d72b1714d38c722a1fe6d78f84ccf0607084d75973c92400197a0f3018a7cc80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:af34734af87c1785082f4ee4526a3ba43d9d2c1780ebd95b45447e450e4c407f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.3 MB (595279077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d468abd55d9624de60cc6525b6e80ca3af7ef848396b5125ccc5c9a00af5024`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 19 Feb 2025 02:55:56 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 19 Feb 2025 02:55:56 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Wed, 19 Feb 2025 02:55:56 GMT
CMD ["gradle"]
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 19 Feb 2025 02:55:56 GMT
WORKDIR /home/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_VERSION=8.12.1
# Wed, 19 Feb 2025 02:55:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04edc0838079d95fa589db479f4ba34a53a5a0224ab75dfa1524aae563c976e1`  
		Last Modified: Thu, 27 Feb 2025 21:08:31 GMT  
		Size: 169.8 MB (169769979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76dacb2f23c45ec295a927c5791597de0b865c2402c463c56a000902cfe65907`  
		Last Modified: Thu, 27 Feb 2025 22:09:13 GMT  
		Size: 163.5 MB (163481874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b9980211333e3801b28018179f297dd75799f3f5fbd1ad186999ae640d3b25`  
		Last Modified: Thu, 27 Feb 2025 22:09:18 GMT  
		Size: 72.3 MB (72262976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadca023eec82c919bd7ce04548e5c0ed67555150f9065f5eb58c6236870a9be`  
		Last Modified: Thu, 27 Feb 2025 22:09:16 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddc0aae67ef110201d27aa939aa6930df7c3940c4efddfaaf4b757386b7aa52`  
		Last Modified: Thu, 27 Feb 2025 22:09:19 GMT  
		Size: 136.6 MB (136610727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d84bab98fd406c35f598ed05d2301d9ccddcea11a58e72f52959cdcff5c5a0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10926012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5fb3e683072b4599cdea71ea5b0d032255b30dbd41d8a0f9ab882eb34a2720`

```dockerfile
```

-	Layers:
	-	`sha256:cb3af0a201ff18ff28a115a942898ed334bfd3e5a26d03b6914908f360f56e84`  
		Last Modified: Thu, 27 Feb 2025 22:09:17 GMT  
		Size: 10.9 MB (10900374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf4f58e7c0788e0f7f5e1238041e7c1e642df92a79224a9347dbc2446c117b03`  
		Last Modified: Thu, 27 Feb 2025 22:09:16 GMT  
		Size: 25.6 KB (25638 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1c3f4078ea1999d82fb73f93fa0870e2cf3a1ca8b878e33d8041d987dd94b101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.5 MB (590491650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f77b0d18c28ba9e5702473ca2e7b181e42c8116b644c69bad8bcd51893bbca6`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 19 Feb 2025 02:55:56 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 19 Feb 2025 02:55:56 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Wed, 19 Feb 2025 02:55:56 GMT
CMD ["gradle"]
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 19 Feb 2025 02:55:56 GMT
WORKDIR /home/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_VERSION=8.12.1
# Wed, 19 Feb 2025 02:55:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:ae97a46dbe642672a09bd4ab6df7280b70a40f641ef4a637aa82879145ebcb67`  
		Last Modified: Sat, 22 Feb 2025 01:44:42 GMT  
		Size: 52.3 MB (52271270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a7fa9126339fcad9127125bfbe77a727d971a2cac1de4cb12df2b202b0e6d1`  
		Last Modified: Thu, 27 Feb 2025 21:22:32 GMT  
		Size: 168.1 MB (168077808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee712be93be9ea53eef663081cafdd413457b11b8c39fe7298f71663f45c6872`  
		Last Modified: Thu, 27 Feb 2025 22:14:12 GMT  
		Size: 161.6 MB (161571427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c43451b7bac075201689bd1985cf60d39e248cf0a9ca9b7f792db10815c016b`  
		Last Modified: Thu, 27 Feb 2025 22:14:10 GMT  
		Size: 72.0 MB (71950568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4905350ba19a1246fbce1706c68bcd72bae03a0bf17a1eb699ea3f5347fb0e`  
		Last Modified: Thu, 27 Feb 2025 22:14:08 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2af40bfdc8395fe7bdaf6f0e68bb2d20e4e225327004a045ac1226d3c7cb3d7`  
		Last Modified: Thu, 27 Feb 2025 22:14:12 GMT  
		Size: 136.6 MB (136618787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:cc78fc3d9693d9c5b7093c3d9f89fc8d9bda64fa0d1dfa5314184cae2787641a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10924137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849f352704868502bf3bd7b05380d328e8401b9ea1552eb7224175d39a4f4bcb`

```dockerfile
```

-	Layers:
	-	`sha256:0cf4d3b21c931f798569e862bad430d5baa3d7d39c697efd3db13f12580507e8`  
		Last Modified: Thu, 27 Feb 2025 22:14:09 GMT  
		Size: 10.9 MB (10898195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:757799219f6e7208cc5f338a6753a2408fc6661044426c1e50ba4f25f15de8f6`  
		Last Modified: Thu, 27 Feb 2025 22:14:08 GMT  
		Size: 25.9 KB (25942 bytes)  
		MIME: application/vnd.in-toto+json
