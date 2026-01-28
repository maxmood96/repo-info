## `gradle:jdk-25-and-25-corretto`

```console
$ docker pull gradle@sha256:102c1e89fcedf164a42ecc95980986960744d8142e05ffe905af6d1ee3c60459
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-25-and-25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:512bd9a2f688585dbf546e9f3dd2bdb3abc1ad83d99ae2f2df2f5fb8e7e56432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.3 MB (466266818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359a7c7e1d09b39f37a9b1de7bea861cd8629fd7f028becd101de55f93cd358e`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:36 GMT
ARG version=25.0.2.10-1
# Tue, 27 Jan 2026 22:13:36 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:13:36 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:13:36 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 27 Jan 2026 23:12:30 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 27 Jan 2026 23:12:30 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 27 Jan 2026 23:12:30 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:12:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:12:30 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:12:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 27 Jan 2026 23:12:30 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:12:30 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:12:30 GMT
ENV GRADLE_VERSION=9.3.0
# Tue, 27 Jan 2026 23:12:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Tue, 27 Jan 2026 23:12:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:12:33 GMT
USER gradle
# Tue, 27 Jan 2026 23:12:34 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 27 Jan 2026 23:12:34 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9307319cf5c73e99e04dcd81f4b9092ff8c453a217e95ba5b67ed0628f3138`  
		Last Modified: Tue, 27 Jan 2026 22:14:01 GMT  
		Size: 189.2 MB (189191158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283e358edcaf0f1570ce3dda33825b84d36e60b63e6bf160ff907f43aa44b6fe`  
		Last Modified: Tue, 27 Jan 2026 23:13:05 GMT  
		Size: 86.0 MB (86035573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae5d9dff75fef54d7c0a73a0af1946744ee666434260bde63f24fa302c2a464`  
		Last Modified: Tue, 27 Jan 2026 23:13:01 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ac9e14e46cabadacf0441fd2dead76fb8f994d7d6d34b7b7d632e59fc3bf8e`  
		Last Modified: Tue, 27 Jan 2026 23:13:06 GMT  
		Size: 137.0 MB (136988871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edbf4c1418279601f9941d446ad99ba76645515f8e8f11449eb5a56b7f4ac84`  
		Last Modified: Tue, 27 Jan 2026 23:13:01 GMT  
		Size: 25.6 KB (25591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a580b8c903530fc5592ec4e5eaaed0c921193efcab263e1543164045b616effc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11367138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d74c1dd0575a83a69d435a81c8713c12c2f96c8f5205fe046cf82909661341`

```dockerfile
```

-	Layers:
	-	`sha256:60a2606051094c02c0627b0d9e35295254086ce47ce91bf3a2c83ae8ab1185f3`  
		Last Modified: Tue, 27 Jan 2026 23:13:02 GMT  
		Size: 11.3 MB (11340661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e760cb6d61907bfe936e88f2beaf73bd5c64e7abe3a87fe2498246d76f798c69`  
		Last Modified: Tue, 27 Jan 2026 23:13:01 GMT  
		Size: 26.5 KB (26477 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-25-and-25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:131c8ff5743737f1d0a35076aaf9398540d305bb157c1b569d65446086071af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.5 MB (462541456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:747fa37442560e274b7a8ff17a60fbb66b62a98f46502c040773d9137f246b54`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:56 GMT
ARG version=25.0.2.10-1
# Tue, 27 Jan 2026 22:12:56 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:12:56 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:56 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 27 Jan 2026 23:11:16 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 27 Jan 2026 23:11:16 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 27 Jan 2026 23:11:16 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:11:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:11:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:11:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 27 Jan 2026 23:11:16 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:11:16 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:11:16 GMT
ENV GRADLE_VERSION=9.3.0
# Tue, 27 Jan 2026 23:11:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Tue, 27 Jan 2026 23:11:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:11:19 GMT
USER gradle
# Tue, 27 Jan 2026 23:11:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 27 Jan 2026 23:11:20 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af45d8028ea21d913fa4bbb3381bedf24377df2182daab5e8ed011f7165bbfd`  
		Last Modified: Tue, 27 Jan 2026 22:13:21 GMT  
		Size: 187.1 MB (187091178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef37029cd7d1994cfb38aeb9e6bbeab596800c0733d18dff573537436961a821`  
		Last Modified: Tue, 27 Jan 2026 23:11:51 GMT  
		Size: 85.5 MB (85513671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafc75d384e4b0f9b0dcaa4293cd1a01bccc093013938368bd1bad6bf4628f46`  
		Last Modified: Tue, 27 Jan 2026 23:11:48 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c3275c29f686f744b5d95931559d0b5f00fb3ba8d03691dddf2eeb51f9cc50`  
		Last Modified: Tue, 27 Jan 2026 23:11:53 GMT  
		Size: 137.0 MB (136988867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a54b053ea4b38ef1a4503539f58677a30ef00c2f244d447735d5693302cfd8d`  
		Last Modified: Tue, 27 Jan 2026 23:11:48 GMT  
		Size: 29.3 KB (29315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:ab83b263303bb8d137a4b77b3257f2395ba6920fc669c6a88e104fd7ff22031e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11366540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7b3b8038bb9c8606712934ef6dabc3913faed7945993c72342ed552f24dbea`

```dockerfile
```

-	Layers:
	-	`sha256:bb30a729c577244310e884ca43914c8952104060eded1385edd3f2c37d265c25`  
		Last Modified: Tue, 27 Jan 2026 23:11:49 GMT  
		Size: 11.3 MB (11339770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4817c92a4451c2951b3fac85bb4b960cdff2fe808fb84e45f39d96d2fd23efa`  
		Last Modified: Tue, 27 Jan 2026 23:11:48 GMT  
		Size: 26.8 KB (26770 bytes)  
		MIME: application/vnd.in-toto+json
