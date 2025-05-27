## `gradle:8-jdk-21-and-24-corretto-al2023`

```console
$ docker pull gradle@sha256:f1dce942600ae5168b0feadcb77127430092078038127c92158124cf51653a1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-21-and-24-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:07424861ed76152ae2039c0343af1505003d8f2206c4f3be8980b8fcb39cac75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.4 MB (606413225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d5a43c44e6fab3741d4fcad9ba5a8a75819fd3bb22154d7a41d775c2b0feea5`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 May 2025 02:26:11 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_VERSION=8.14.1
# Tue, 27 May 2025 02:26:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Wed, 14 May 2025 01:42:44 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1dd26f3fd48ad2bdc7fb164ac55c6714a2039d97013de0c5f2b15de0d74ec1`  
		Last Modified: Mon, 19 May 2025 23:37:14 GMT  
		Size: 169.8 MB (169833486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d712d7e73b64e078c67ade3696bdcb769937371166dc60a6288c4b7e521497d`  
		Last Modified: Tue, 27 May 2025 18:59:46 GMT  
		Size: 173.1 MB (173078931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df83384924953f5fca13e4113ad4a6d6a585e68ba5919a9f13efa1f9a95532f3`  
		Last Modified: Tue, 27 May 2025 18:59:44 GMT  
		Size: 72.4 MB (72432561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f8dc968e879320cbb9e2062f14d2ae0987761fecd8be0a02b12ecb47f0208a`  
		Last Modified: Tue, 27 May 2025 18:59:42 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c20f35029631521c08ba049e4455cb4640a2691c72afea35741a2a89d3d4eb`  
		Last Modified: Tue, 27 May 2025 18:59:45 GMT  
		Size: 137.5 MB (137451757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a128ea6b956dfa379e410605ee22a11c73e13d5f2cae77498eb86f9ff6d0919c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10992956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7310d040938cc76f40f39a252876a2372ec84c08b9d4929bbc52929c3aa97a`

```dockerfile
```

-	Layers:
	-	`sha256:6fdff5dc393a1d68f1c025d2c875e263a2b1ef5d75bd79aecd27462760b20627`  
		Last Modified: Tue, 27 May 2025 18:59:42 GMT  
		Size: 11.0 MB (10967318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79b9327be646578b4347496c6e2924b282940cca7c59083ee09aa244753f509`  
		Last Modified: Tue, 27 May 2025 18:59:43 GMT  
		Size: 25.6 KB (25638 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-24-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b6eb7b83578583089462d231375c83d851c4c643ba9b9abe5641572a1b0bceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.4 MB (601357547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d05bd8703389fd37de3fe7ac0c94c88e9fa8398edecdc7ce4ba0d0703d6c14f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 May 2025 02:26:11 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 27 May 2025 02:26:11 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 27 May 2025 02:26:11 GMT
CMD ["gradle"]
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 May 2025 02:26:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 27 May 2025 02:26:11 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 May 2025 02:26:11 GMT
WORKDIR /home/gradle
# Tue, 27 May 2025 02:26:11 GMT
ENV GRADLE_VERSION=8.14.1
# Tue, 27 May 2025 02:26:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
# Tue, 27 May 2025 02:26:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=845952a9d6afa783db70bb3b0effaae45ae5542ca2bb7929619e8af49cb634cf
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Wed, 14 May 2025 01:42:43 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd140d5ff7cfeed9c5da7c3591b30e13df8be78b63c8efafddcaf1920a14be7`  
		Last Modified: Tue, 20 May 2025 00:01:28 GMT  
		Size: 168.1 MB (168137719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faa978ee91834970e9a84411f18d1901f7b43803fb6242d5a36a6fbd3d19fc7`  
		Last Modified: Tue, 27 May 2025 20:06:00 GMT  
		Size: 171.2 MB (171171355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e32b84bc022caabcbf9a1c927a9a9f8ec50918d9fc9997d24d812912b38742`  
		Last Modified: Tue, 27 May 2025 20:05:58 GMT  
		Size: 72.0 MB (72023695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c153fdc51e086440de8280711231e91831ff1f21612542e1346cc98197c8fc1f`  
		Last Modified: Tue, 27 May 2025 20:05:55 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d1d3c0535bf8c2e6c234aa1e80dffa1bb0c8bb7ccac00919bc086445789520`  
		Last Modified: Tue, 27 May 2025 20:05:59 GMT  
		Size: 137.5 MB (137457252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:11d3597a2abbe0ec029193f126cf11a7b68db351d0d9523e7d796823a1c3bddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.0 MB (10991718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2703a3b8421e3836053167e2029cd2bddd02ea55108c467d6f72034e2ff6a3`

```dockerfile
```

-	Layers:
	-	`sha256:260e2fef18a27be49bcef7016281a06e54e740eca1bd3ff6214272f4c6eb69ec`  
		Last Modified: Tue, 27 May 2025 20:05:56 GMT  
		Size: 11.0 MB (10965776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4db886f2a63f457069c9a595645520163fa2738ae1660aac840a884e6739965`  
		Last Modified: Tue, 27 May 2025 20:05:55 GMT  
		Size: 25.9 KB (25942 bytes)  
		MIME: application/vnd.in-toto+json
