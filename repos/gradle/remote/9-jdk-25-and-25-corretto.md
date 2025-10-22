## `gradle:9-jdk-25-and-25-corretto`

```console
$ docker pull gradle@sha256:4618ddd1bc6950541bcb24c266e89cd30c053aad4a6883ec40b6a7816014f224
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:b3aa9f528bd0cec83d3ab82d4900cfcfc2aec6fdf23b0518ea4da3b61ad4ba6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.3 MB (463274039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df0fe59eff941d27e77411712851b0f6633da988a84b8cbee431f2db67750eb`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306660de4f7e21947211b947419c44cd0a88b1b2e458d0cf71d9a51d2b9e6f21`  
		Last Modified: Mon, 06 Oct 2025 22:10:06 GMT  
		Size: 189.1 MB (189134226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8c2a68a841fe0568a195fe9439b9e108eb8ac3b5f64aae2ae17e1364e50d1d`  
		Last Modified: Mon, 06 Oct 2025 22:12:06 GMT  
		Size: 85.6 MB (85560166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718e86b164c1e2ecbcd25b3990a3dd88701a080b1db9b101ed32c9fd0e1cc2ce`  
		Last Modified: Mon, 06 Oct 2025 22:12:00 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c159819434dc258ed46dc1afe1149eb61cb69dc382a085af1daddfed496686d8`  
		Last Modified: Mon, 06 Oct 2025 22:59:04 GMT  
		Size: 134.6 MB (134572728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:791964c090fe8f8dc0848a26c9148c47722ce46bada992d01b67c00980b0afa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11341023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f30d41f002839dbfbe77313d15a70d77821bd31cfe6cda2f1eac4a1dcad17c`

```dockerfile
```

-	Layers:
	-	`sha256:6fce02ae7c39a493316763898e78420984856021f2e56b3d64b951bbf36fce0e`  
		Last Modified: Mon, 06 Oct 2025 23:23:24 GMT  
		Size: 11.3 MB (11316541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab78e0956f8ebd3873f0b0b21be8310db48b63c9be0757de8476a24a1e99bd24`  
		Last Modified: Mon, 06 Oct 2025 23:23:25 GMT  
		Size: 24.5 KB (24482 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:67464f2ac7bdc6cf5630fcf7af80a615f257a634f5546480b2697c27c503d18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.7 MB (459655548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6a61bffd3eaccc8c4bc641bb4b686282886017768e965b73d72acf95af5f79`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 30 Sep 2025 09:31:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["/bin/bash"]
# Tue, 30 Sep 2025 09:31:25 GMT
ARG version=25.0.1.8-1
# Tue, 30 Sep 2025 09:31:25 GMT
ARG package_version=1
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
ENV LANG=C.UTF-8
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0facfa421fa0d39948514b8fdbe1af18c63525acb19c3f4c8bddc6d0d119af`  
		Last Modified: Tue, 21 Oct 2025 22:11:05 GMT  
		Size: 187.1 MB (187096320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f4138e78726675eec26a9325dab512ae8f14c9a07e081c08032c29e01ae5d`  
		Last Modified: Tue, 21 Oct 2025 22:12:52 GMT  
		Size: 85.1 MB (85088723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6628f69582569ca775141b534e5b73157435040eba3c3449a5dff70cd6b940c6`  
		Last Modified: Tue, 21 Oct 2025 22:12:47 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cd549d2f3274d841800e164fa17c14ec6ef503e58079de08272019f7fbe111`  
		Last Modified: Wed, 22 Oct 2025 03:33:17 GMT  
		Size: 134.6 MB (134577518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:dc6ff60546334dc7f50b351673163d8ed4e8cfd47bb24a3c491ac76248d13774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11340408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb585a1fa22ede6be8746a88faca21ffc38264fbaf7ed5086e1f78b2dae96854`

```dockerfile
```

-	Layers:
	-	`sha256:aa5c9fe1870716699d58c53fe38dd20ef1d7c9a072f1775e3713e333190eb444`  
		Last Modified: Tue, 21 Oct 2025 23:22:44 GMT  
		Size: 11.3 MB (11315648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5cc14d7a22f5095e57df4eeee7ec23aeb5ce8060afc7d1734d41606097877dc`  
		Last Modified: Tue, 21 Oct 2025 23:22:45 GMT  
		Size: 24.8 KB (24760 bytes)  
		MIME: application/vnd.in-toto+json
