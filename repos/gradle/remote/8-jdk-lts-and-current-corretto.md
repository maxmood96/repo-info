## `gradle:8-jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:1b4e8325046ac2fedf633430f0474fa5d5cd36269a1560e37e42a1eff3e6e1c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:30c8019190614555a2ea01a9ef9f13efb861bbf00730495de70884ca07a50363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.6 MB (593642027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc96c4036716891104f28eaaa7db01b72597af1cd6d9e59dc3079c9bf92d9e9b`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 20 Dec 2024 17:54:11 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 20 Dec 2024 17:54:11 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Fri, 20 Dec 2024 17:54:11 GMT
CMD ["gradle"]
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 20 Dec 2024 17:54:11 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Dec 2024 17:54:11 GMT
WORKDIR /home/gradle
# Fri, 20 Dec 2024 17:54:11 GMT
ENV GRADLE_VERSION=8.12
# Fri, 20 Dec 2024 17:54:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Fri, 20 Dec 2024 17:54:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7cd1ddb95c1ab4ae8c9a6cb4c02e3f8eb17e4afe0942c11f465c105cedafea`  
		Last Modified: Fri, 20 Dec 2024 22:33:30 GMT  
		Size: 169.8 MB (169755700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bb0342f61dfcf482beaa04368116f55b37fee3777181311f2b80f6747cd452`  
		Last Modified: Fri, 20 Dec 2024 23:15:12 GMT  
		Size: 163.5 MB (163457108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9ac83c535de8363f670974825d16c258f62625a17c9d20a9c80389edd0c31b`  
		Last Modified: Fri, 20 Dec 2024 23:15:11 GMT  
		Size: 70.7 MB (70659377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29789cfcf1a3a22a75fe920af4eb1a20ac473e65d9673dd97c4cfdc9def528a`  
		Last Modified: Fri, 20 Dec 2024 23:15:10 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781d4adf60a4cb43488b773a0078653e3884cedd3733d0893b25d17ed4684e02`  
		Last Modified: Fri, 20 Dec 2024 23:15:13 GMT  
		Size: 136.6 MB (136611742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d7a2bb625d61189573c0ccf5a66e09d2a1327ba37adb255d57a71f5c577a6079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10905938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35a1023a85c1c3a29d89d42fc292ea3ac4a15865da90acda4b8bea73850f31b`

```dockerfile
```

-	Layers:
	-	`sha256:db0b5382b9a1fe6affc5423981e561e92abc554b7733b94f2bcc9f50349272e4`  
		Last Modified: Fri, 20 Dec 2024 23:15:11 GMT  
		Size: 10.9 MB (10880303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47cba05458ef57cddb6c55f1e7f97a8b5f2636a67a1f129ae8e495a5bf782cb5`  
		Last Modified: Fri, 20 Dec 2024 23:15:10 GMT  
		Size: 25.6 KB (25635 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0b3296226e561088c7869f0b12852bc206b9e033424dcde5ad674ef5f3ffd6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.2 MB (588220910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b43eb2cf72838846fc2d3c278d1114bdd9410b48618b72e2c23b27bb6bf195`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 20 Nov 2024 19:11:06 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 20 Nov 2024 19:11:06 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Wed, 20 Nov 2024 19:11:06 GMT
CMD ["gradle"]
# Wed, 20 Nov 2024 19:11:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 20 Nov 2024 19:11:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 20 Nov 2024 19:11:06 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 20 Nov 2024 19:11:06 GMT
WORKDIR /home/gradle
# Wed, 20 Nov 2024 19:11:06 GMT
ENV GRADLE_VERSION=8.11.1
# Wed, 20 Nov 2024 19:11:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=f397b287023acdba1e9f6fc5ea72d22dd63669d59ed4a289a29b1a76eee151c6
# Wed, 20 Nov 2024 19:11:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f397b287023acdba1e9f6fc5ea72d22dd63669d59ed4a289a29b1a76eee151c6
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:c4986d7f39b7bf5efc7dcb24fad3d45645e69ad032505693865ef726c1550fb5`  
		Last Modified: Sat, 23 Nov 2024 01:38:05 GMT  
		Size: 51.5 MB (51455844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f38ff443b6dbbe50c39fe5e28664a701d1d9ef37e7260734f9c881393c8908`  
		Last Modified: Mon, 02 Dec 2024 23:28:52 GMT  
		Size: 167.9 MB (167938069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28721539daa784fa661b479317a3bb42ab1387575fcbf4f90f423d5d776ac2df`  
		Last Modified: Tue, 03 Dec 2024 00:30:36 GMT  
		Size: 161.5 MB (161485769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b69e6ba5cd9a4b6d8e2c04be05665ccb0ddff812206c1d931e0978784996f8`  
		Last Modified: Tue, 03 Dec 2024 00:30:34 GMT  
		Size: 70.4 MB (70356760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daeb175ca0aa1303b7bc88c30fa772139ea980fd5f9fa2462b4214896f4cc703`  
		Last Modified: Tue, 03 Dec 2024 00:30:32 GMT  
		Size: 1.8 KB (1753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb7cf101e993097d2a38e430593523f09f42daa53fa32fab07d6d068105870b`  
		Last Modified: Tue, 03 Dec 2024 00:30:37 GMT  
		Size: 137.0 MB (136982683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e09d1ebd9f4b81628e1c922e97deceb0addabc68dabd641a0c5973dfa0c9287d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10928140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc502f7119787cdf0c9d930333cdbbfb4dce63c3b346c0df5ca0552dc5fba3ac`

```dockerfile
```

-	Layers:
	-	`sha256:6b6fdf65dc56c9799bebe08521a2848639891bbacc455d5df0468b20e4026c12`  
		Last Modified: Tue, 03 Dec 2024 00:30:33 GMT  
		Size: 10.9 MB (10902198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb3ca2911debafa6eee34284d76efab68251a2ade70c481eb45e51f280f0b03`  
		Last Modified: Tue, 03 Dec 2024 00:30:32 GMT  
		Size: 25.9 KB (25942 bytes)  
		MIME: application/vnd.in-toto+json
