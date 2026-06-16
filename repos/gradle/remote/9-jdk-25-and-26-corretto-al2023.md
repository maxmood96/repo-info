## `gradle:9-jdk-25-and-26-corretto-al2023`

```console
$ docker pull gradle@sha256:2bc98330969a98253653b5a11b89d15436b7f2a99facf7fc7306bc0769be0e8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-26-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:c57660358682e5530e5c387cbb0a6645c3803d8d302ce24ccc44e831544b1074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.8 MB (649763392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce89b61606f0cc4de5ba7fde1c293a5f618f2861ee64822fe1b5adf76eadd66`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:15 GMT
ARG version=25.0.3.9-1
# Tue, 16 Jun 2026 01:16:15 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:15 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:15 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 16 Jun 2026 02:19:26 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Tue, 16 Jun 2026 02:19:44 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 16 Jun 2026 02:19:44 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 16 Jun 2026 02:19:44 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:19:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:19:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:19:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 16 Jun 2026 02:19:45 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:19:45 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:19:45 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 16 Jun 2026 02:19:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 16 Jun 2026 02:19:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:19:47 GMT
USER gradle
# Tue, 16 Jun 2026 02:19:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 02:19:47 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd44d40bd5b8f538bd043478c7f8bfcafc04f3a3a27b15f9231ff3acd91c7a8`  
		Last Modified: Tue, 16 Jun 2026 01:16:40 GMT  
		Size: 189.4 MB (189412755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dae3799142a1902eaf9978020b4e8b0e76dd279a58806d746bfea78851811d`  
		Last Modified: Tue, 16 Jun 2026 02:20:25 GMT  
		Size: 179.2 MB (179247379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6aaf3de51f13329ccb919a56f771c909637ea2a4d9701dde0c2a270af49eff9`  
		Last Modified: Tue, 16 Jun 2026 02:20:22 GMT  
		Size: 86.3 MB (86267723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88393b6ace163fcf71569d9716d4c7024e0e0cc0c59165339c35455b9bfc06d9`  
		Last Modified: Tue, 16 Jun 2026 02:20:17 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e79fb2222931a261eded7701805d6ffcb6abc290cc5c4d7973efe5366e7a2e`  
		Last Modified: Tue, 16 Jun 2026 02:20:24 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3d130ad78f2d2c84ac1f066df6ee960e6dd4079fa3ae7c0238895b67cddb8e`  
		Last Modified: Tue, 16 Jun 2026 02:20:18 GMT  
		Size: 25.6 KB (25603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:22564f60c9046bec93eef6c776704ac03dcdbfd6b35b2e77b6721a5f641a7f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11574154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600f64a14eba68ac485cbdc886f34da3e500a3f9c23eaae37125b21d688c0acd`

```dockerfile
```

-	Layers:
	-	`sha256:512332cdfd1276522aa1c9a4a233219e7e71ee00d30457083c8aa78710224a04`  
		Last Modified: Tue, 16 Jun 2026 02:20:18 GMT  
		Size: 11.5 MB (11544645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:705e266354f906ea33422a57eefa4434dd7fd7c0ac0eee21bc99f5ecc8fe1428`  
		Last Modified: Tue, 16 Jun 2026 02:20:17 GMT  
		Size: 29.5 KB (29509 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-26-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9344361568f7821995397ef0988cef9f256c5763d623b680330a5865345c3ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.9 MB (643898752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d2962de54af522df21e978992c2f0765d94f11013a604b639893a9b8f010be`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:17:31 GMT
ARG version=25.0.3.9-1
# Tue, 16 Jun 2026 01:17:31 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:17:31 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:17:31 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:17:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 16 Jun 2026 02:20:01 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Tue, 16 Jun 2026 02:20:25 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 16 Jun 2026 02:20:25 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 16 Jun 2026 02:20:25 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:20:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:20:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:20:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 16 Jun 2026 02:20:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:20:26 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:20:26 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 16 Jun 2026 02:20:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 16 Jun 2026 02:20:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:20:28 GMT
USER gradle
# Tue, 16 Jun 2026 02:20:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 02:20:29 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9225181157827e8afe6b6e29e476737d88a7af31a53eb9317eb2c87ab556b1a3`  
		Last Modified: Tue, 16 Jun 2026 01:17:56 GMT  
		Size: 187.3 MB (187327596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d690500b1dae589c689d9d60fc2231d840129749a7a5faa3346b787f370dbf08`  
		Last Modified: Tue, 16 Jun 2026 02:21:13 GMT  
		Size: 177.1 MB (177119326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a8f46199072910d80af2148715bba4c1fc1b563cb0ba127f8b4e33abca718c`  
		Last Modified: Tue, 16 Jun 2026 02:21:09 GMT  
		Size: 85.7 MB (85725893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4050da40da6233f765567c8478a8dc9a60bd8b98658a9f769a74b25b76e776a`  
		Last Modified: Tue, 16 Jun 2026 02:21:02 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0876206f8bc4bbd5cac9bd78f5ed6d981c5a660f519bd16a7c7a3f0f818bcccf`  
		Last Modified: Tue, 16 Jun 2026 02:21:13 GMT  
		Size: 140.2 MB (140236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b982c13a178a219d9becc5a2239dd398d99adbb14fe77636a115f03ab0c5ca8`  
		Last Modified: Tue, 16 Jun 2026 02:21:03 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:f2a70aea684e712e8fd940e416fc13c89e662e22ea56d00bf57c47dff3ec3b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11572944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31eac45904fb85d2794cf77eb03828b0cca05bd185ba877c3e47e97fb7017610`

```dockerfile
```

-	Layers:
	-	`sha256:7b257e2c0a6ec825946b5aef8783028aeba9d7e99eb2d3a3e7db0688d921b00b`  
		Last Modified: Tue, 16 Jun 2026 02:21:03 GMT  
		Size: 11.5 MB (11543115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35dc797ee67886cb7282a48e326e10d07981e604ddf64e360bd95d7b70dd3958`  
		Last Modified: Tue, 16 Jun 2026 02:21:01 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json
