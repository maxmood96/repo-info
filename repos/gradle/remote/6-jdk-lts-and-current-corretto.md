## `gradle:6-jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:f16af11fe5e26e6018715d17d4b86757c36e36518fadbc619642a53b5851dc14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:577380d6c738230bd43e39672f4f791d13ea6296d639a9616e46faf16c1a9d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **566.8 MB (566794739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20aaf9b4f5582f119ac2d9b0f8cd9e9e0449bc16f7eb06cb2157ef87a4eede0`
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
# Tue, 18 Feb 2025 21:10:38 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Feb 2025 21:10:38 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
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
	-	`sha256:1772c34207885a264e0a3ab94d223855bf2ffb16546733bc1daa1914db78b23d`  
		Last Modified: Thu, 27 Feb 2025 22:09:11 GMT  
		Size: 72.3 MB (72263013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbbee993271b08195cfbb930df2257c06aadb1f6af7915bd423aa558a610618`  
		Last Modified: Thu, 27 Feb 2025 22:09:10 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411bdb1786abd4464361eeba37a959792a53f72ead96be443611b5942ba991b4`  
		Last Modified: Thu, 27 Feb 2025 22:09:12 GMT  
		Size: 108.1 MB (108126353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3396cd7e3ac5e4b7b04ec68fc4df445bd0a6a53a70a362b7f068cc392628159e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10824893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bb9a3986d551c5bc445a9c2545e9ee0c6a55115b25249016e4f28a47f38e73`

```dockerfile
```

-	Layers:
	-	`sha256:a13512b7ad28de68f503e8a08cea8739a495a670e6fb7abe698d0c217456ec05`  
		Last Modified: Thu, 27 Feb 2025 22:09:10 GMT  
		Size: 10.8 MB (10800644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2dd64433b517c4cd5ba2c30941cb98a80c72616942dd8627cc0addb65615842`  
		Last Modified: Thu, 27 Feb 2025 22:09:10 GMT  
		Size: 24.2 KB (24249 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:77adea91671f7bf016a2fa83090f13f718121585fce54e978203b91930135758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **562.0 MB (561993460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3aaf9cffb4a098bade3e10fe4885766b300f932d72210b29935dbbb9808955a`
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
# Tue, 18 Feb 2025 21:10:38 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Feb 2025 21:10:38 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 18 Feb 2025 21:10:38 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 18 Feb 2025 21:10:38 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:38 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:38 GMT
ENV GRADLE_VERSION=6.9.4
# Tue, 18 Feb 2025 21:10:38 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Tue, 18 Feb 2025 21:10:38 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
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
	-	`sha256:ba7bb614aad90cfa55a09b378a5017aad6dfa59ee5b059df9d54119185dfa8a5`  
		Last Modified: Thu, 27 Feb 2025 22:22:53 GMT  
		Size: 108.1 MB (108120597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:064295c5995b13af2fbd2f507e19d4df804c8a4e53b0e923b3896bba6522ca80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10822920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb59b7f497b1ad46b7c002d2e9d66c04d7ad2a133308260fe53f9084de4518e`

```dockerfile
```

-	Layers:
	-	`sha256:7eed41bf2147ccb9e290a1104ab5c78c55843dc67ee5626fa4d075291d8f2170`  
		Last Modified: Thu, 27 Feb 2025 22:22:50 GMT  
		Size: 10.8 MB (10798417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6da84afa9cf258fa31a7d9a5b8a02e51ccb4736b09b2653f2b3476cac3cbdbf`  
		Last Modified: Thu, 27 Feb 2025 22:22:49 GMT  
		Size: 24.5 KB (24503 bytes)  
		MIME: application/vnd.in-toto+json
