## `gradle:jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:a7d2c905737825e030ddd2c6c2b8eb1f98cbc65a34a7d2dd2348f01e6b314d02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:18cb41a349c9ab3a192ce8b637a609f10cfdba5162736f986704113957e791a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.8 MB (649763317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d569fd7d1171eb3d42ed07b0a167d2d2def63889de2a59e64ea3eefdf9ccd789`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:42 GMT
ARG version=25.0.3.9-1
# Tue, 09 Jun 2026 21:12:42 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:42 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 09 Jun 2026 22:05:05 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Tue, 09 Jun 2026 22:05:24 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 09 Jun 2026 22:05:24 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 09 Jun 2026 22:05:24 GMT
CMD ["gradle"]
# Tue, 09 Jun 2026 22:05:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 09 Jun 2026 22:05:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 09 Jun 2026 22:05:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 09 Jun 2026 22:05:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 09 Jun 2026 22:05:25 GMT
WORKDIR /home/gradle
# Tue, 09 Jun 2026 22:05:25 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 09 Jun 2026 22:05:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 09 Jun 2026 22:05:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 09 Jun 2026 22:05:27 GMT
USER gradle
# Tue, 09 Jun 2026 22:05:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 09 Jun 2026 22:05:27 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2cff886cd8efbaaf67f0b1d3449b228936c361c65f92f96e99b501f9431ebf`  
		Last Modified: Tue, 09 Jun 2026 21:13:07 GMT  
		Size: 189.4 MB (189412731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042dc452004a48893070e5dc36d5cb402a35afb3c3bb7b1df927341ca750ef34`  
		Last Modified: Tue, 09 Jun 2026 22:06:07 GMT  
		Size: 179.2 MB (179247394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047e749a35e9164961f3f68c3478811c529c05a38b0afe7e690fc569c8504799`  
		Last Modified: Tue, 09 Jun 2026 22:06:04 GMT  
		Size: 86.3 MB (86267657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e348c8cbb391c4a955af7c553c9d1938389658434388d911f6827b27100120`  
		Last Modified: Tue, 09 Jun 2026 22:05:59 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac34a04763fa14a5efe5e1ae3b0784cb9764e8fbbeb9c4a93615fab34fc11a7d`  
		Last Modified: Tue, 09 Jun 2026 22:06:06 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39bfa360976092d7144a9055e015f9669ad6fcf87abf7ad69eef4e08183cae98`  
		Last Modified: Tue, 09 Jun 2026 22:06:01 GMT  
		Size: 25.6 KB (25603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:be86c15acc2648a23b5372e33540667bd2d6d931a71c413670420d21dada746f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11574153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6e2aa0a7993c06acb3c53bdc885feeda1cc02bffc9c8d01517380ed0742effe`

```dockerfile
```

-	Layers:
	-	`sha256:5fd0b126422651d0effc46c65b988ba8f3461aa245bc32bc2e5abd39cbf58eda`  
		Last Modified: Tue, 09 Jun 2026 22:06:00 GMT  
		Size: 11.5 MB (11544645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c2a106e872d2f97bd6c03f054a1cd7753460d8a97d0fbe059fd2fd9735e268`  
		Last Modified: Tue, 09 Jun 2026 22:05:59 GMT  
		Size: 29.5 KB (29508 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:90bda6fa086031407ddd9c383c64915b37fd6de832d4346e85ae449747bd1278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.9 MB (643897903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa3ea902aa47711c17807ea3e6b7439eee10938c6d94e90956e22b0edc8d011`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:37 GMT
ARG version=25.0.3.9-1
# Tue, 09 Jun 2026 21:12:37 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:37 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:37 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 09 Jun 2026 22:06:32 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Tue, 09 Jun 2026 22:06:55 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 09 Jun 2026 22:06:55 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 09 Jun 2026 22:06:55 GMT
CMD ["gradle"]
# Tue, 09 Jun 2026 22:06:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 09 Jun 2026 22:06:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 09 Jun 2026 22:06:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 09 Jun 2026 22:06:55 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 09 Jun 2026 22:06:55 GMT
WORKDIR /home/gradle
# Tue, 09 Jun 2026 22:06:55 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 09 Jun 2026 22:06:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 09 Jun 2026 22:06:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 09 Jun 2026 22:06:58 GMT
USER gradle
# Tue, 09 Jun 2026 22:06:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 09 Jun 2026 22:06:58 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62292040f1e97bc790fd253e8fd7ba92295a350f31be03f2f532387f78e3d3f1`  
		Last Modified: Tue, 09 Jun 2026 21:13:04 GMT  
		Size: 187.3 MB (187327258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a9b718ce2a869fb8c30faa74531d0a41b2fee29fe3db0fa6f564eee05c4dda`  
		Last Modified: Tue, 09 Jun 2026 22:07:38 GMT  
		Size: 177.1 MB (177119373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfdab1d00d9492c65b7ea4ebd5a746eba99cf250c71bffc67349e3a0fd1d3fa`  
		Last Modified: Tue, 09 Jun 2026 22:07:35 GMT  
		Size: 85.7 MB (85725339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480c1637fc2001ab12b9a1eba4c74863c2b3474855fe9f3d5889cf0f2339c926`  
		Last Modified: Tue, 09 Jun 2026 22:07:30 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9c198214c79b70482e973531ea29089e157155da7049d4ae118a2f55e738a8`  
		Last Modified: Tue, 09 Jun 2026 22:07:38 GMT  
		Size: 140.2 MB (140236982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a239934e6b510b3bc0c2b749e486bbad1186a2a7b1116968c380081e52ebfc`  
		Last Modified: Tue, 09 Jun 2026 22:07:32 GMT  
		Size: 29.3 KB (29333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bb8d41caeca7409aa578c150ca2315043e575f8bc5a5a6578bee45937dbb000e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11572944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d833aa6654817f2ef0d84efea2098740e2c4b092b7820fe83a111bbe3f201d48`

```dockerfile
```

-	Layers:
	-	`sha256:36e4c550bcf2f9e8c43d359a581e09e189dec9e0d8073e091002748207499875`  
		Last Modified: Tue, 09 Jun 2026 22:07:31 GMT  
		Size: 11.5 MB (11543115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbba9364e8ab55c75742a1a50e8b3e8f9fd24adbe104ecb71e05944c39874273`  
		Last Modified: Tue, 09 Jun 2026 22:07:30 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json
