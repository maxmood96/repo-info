## `gradle:jdk-25-and-25-corretto`

```console
$ docker pull gradle@sha256:a3fe29618683522ef51dfb6c8ca621da27560fed28b76e24a0e58304801aa75b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-25-and-25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:87fe7a3e65b3a859fd1052f4f4f1a5c9a9a95c84e725ba54ad3050a6367bf1a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.1 MB (467093647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b264e707e386b515e1de0558cb340032116c4d8f2cab2dc2f032a4692dabc22`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:25 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:25 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:25 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:25 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 11 Mar 2026 19:13:01 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 11 Mar 2026 19:13:01 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 11 Mar 2026 19:13:01 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:13:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:13:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 11 Mar 2026 19:13:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 11 Mar 2026 19:13:01 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:13:01 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:13:01 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 11 Mar 2026 19:13:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 11 Mar 2026 19:13:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:13:04 GMT
USER gradle
# Wed, 11 Mar 2026 19:13:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 11 Mar 2026 19:13:04 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1899f99dbf61d2e92bf9bc374b2f4ec7c5b8a1687b8543b4ecc212164833f14`  
		Last Modified: Wed, 11 Mar 2026 18:34:50 GMT  
		Size: 189.2 MB (189186371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419c251b128bd486bed665202dd6573d21fd3856003c4037fe824db8c897eed0`  
		Last Modified: Wed, 11 Mar 2026 19:13:33 GMT  
		Size: 86.1 MB (86073627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30700a23c3499667922a2dd20c1123525725beee3c82e372c9dbeac0e210cae`  
		Last Modified: Wed, 11 Mar 2026 19:13:29 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3abf15ee6bec1c92f670ecd1bc9033e07bf78438b6580e1d0e4a1cccf5c7799`  
		Last Modified: Wed, 11 Mar 2026 19:13:35 GMT  
		Size: 137.8 MB (137773160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55d20b90040e7e8257c3b99fe213a2a3436fe0efbd13ab43cbadef4d8178119`  
		Last Modified: Wed, 11 Mar 2026 19:13:29 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:26a48f3425a35fcbfbe7dbe017303100f341198961be34b6ad8e0ee64f57705a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fb5d32fd79d5c5b658f0e9e5eeea55f85499d86347852ff22caddda56d5ea8`

```dockerfile
```

-	Layers:
	-	`sha256:3ab6828dc24bba6c4cf68b22c3828419eab886473f6bcd8be2cc18d67ed6d00a`  
		Last Modified: Wed, 11 Mar 2026 19:13:30 GMT  
		Size: 11.3 MB (11343297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17650c07bf8213dfa3ad3052d8735391b643effd028f99c0a9f7bc8f897db26`  
		Last Modified: Wed, 11 Mar 2026 19:13:29 GMT  
		Size: 26.5 KB (26475 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:175f262efdb93b5389eb650746c3ff5303fe9acdc38e2951d4ef7a46a422b08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463379856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a118e9b7e8d7cb9696568c8ce933f091f518a610a7862cf7b6d8b02985283d1d`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:05 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:05 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:05 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:05 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 11 Mar 2026 19:13:12 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 11 Mar 2026 19:13:12 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 11 Mar 2026 19:13:12 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:13:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:13:12 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 11 Mar 2026 19:13:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 11 Mar 2026 19:13:12 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:13:12 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:13:12 GMT
ENV GRADLE_VERSION=9.4.0
# Wed, 11 Mar 2026 19:13:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
# Wed, 11 Mar 2026 19:13:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:13:15 GMT
USER gradle
# Wed, 11 Mar 2026 19:13:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=60ea723356d81263e8002fec0fcf9e2b0eee0c0850c7a3d7ab0a63f2ccc601f3
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 11 Mar 2026 19:13:16 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9ab420359a2ce38b24b838a3ea4b4bcbfe85a0c06909eead4a8cca721947cb`  
		Last Modified: Wed, 11 Mar 2026 18:34:30 GMT  
		Size: 187.1 MB (187088807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259277d2e2e5d35ccdd6db6da18e8128e0d8fadb3bf0685354cb151a4fa6f4fc`  
		Last Modified: Wed, 11 Mar 2026 19:13:47 GMT  
		Size: 85.5 MB (85545388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a7af9d7fc0c8a17641d17de15f6826e9972caf01e0904180cb7ce3be580449`  
		Last Modified: Wed, 11 Mar 2026 19:13:44 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a203f203dd05e7bfbc1c641e156dcf4a0be91188517a27838e0a729289ed3de`  
		Last Modified: Wed, 11 Mar 2026 19:13:49 GMT  
		Size: 137.8 MB (137773157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57297e9afa597dd6e2fe27cbcc2f39c7bb3773e48924179c285610ace185cefe`  
		Last Modified: Wed, 11 Mar 2026 19:13:44 GMT  
		Size: 29.3 KB (29341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5506fe3ff622ee15064a7df4e80060b56bfbd16a02ae2b53959b39a4bd64b1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11369176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e948c9dd133f4857a2f383bec0b64b328e5b4770fbdd0cecf8e6e29e89ca581a`

```dockerfile
```

-	Layers:
	-	`sha256:66296057c78846687bb535e9f7ab7dc7a84bf83976e681d1f71216a4f621a60f`  
		Last Modified: Wed, 11 Mar 2026 19:13:45 GMT  
		Size: 11.3 MB (11342406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629ed4b3284938257d20c68f80d5c321b0b5e07807007a7b0235872fb24cccbd`  
		Last Modified: Wed, 11 Mar 2026 19:13:44 GMT  
		Size: 26.8 KB (26770 bytes)  
		MIME: application/vnd.in-toto+json
