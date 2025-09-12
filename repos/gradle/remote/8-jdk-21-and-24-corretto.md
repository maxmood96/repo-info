## `gradle:8-jdk-21-and-24-corretto`

```console
$ docker pull gradle@sha256:95d364574f0958a9f9e5e020086c2bd24ac4f54576ebd246e1390499f8a1b198
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-21-and-24-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:6d2aa2a2177125d33affb45a6d24a712b4c6f42f3e1a8aa446c64de18882110c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **620.1 MB (620137797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:225b67caf42f49e430a72b6268a76deafb4eece80ff0521d70cfd367c5955667`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=21.0.8.9-1
# Thu, 17 Jul 2025 03:50:10 GMT
ARG package_version=1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b277a99eedd058e5435ee84d1bf1db6bfc8c7b5b9a602de4fe6a22df9fc96cb`  
		Last Modified: Fri, 12 Sep 2025 02:10:37 GMT  
		Size: 170.1 MB (170108136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1659d392b1376c65128ea1439c188d0500663dd89e53a0c9814bd5f76f161100`  
		Last Modified: Fri, 12 Sep 2025 09:03:19 GMT  
		Size: 173.1 MB (173149177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45373b8e65c624ff88e30bdc65ca7f4862aacfb4efcf5082d6af41ca3bbd0d63`  
		Last Modified: Fri, 12 Sep 2025 02:12:15 GMT  
		Size: 85.6 MB (85551581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690cdb528a32c33ce5ca68f92dcc06be075bf8f70ffa91f285d5fd1fb60f3b85`  
		Last Modified: Fri, 12 Sep 2025 02:52:45 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfc0c28e26849e324741c42f4e9e7a68bfbbd1bc278a54e59a259f7dfe7d290`  
		Last Modified: Fri, 12 Sep 2025 09:03:35 GMT  
		Size: 137.5 MB (137451408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:755c1c47a34503e9b555a8d3613408e496d2f179d10a133d7b4abe36caf24197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11506670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73da3b7038e0248f8076339985d2f5d1b2b7e09f31bc03324c03f335f016c5a7`

```dockerfile
```

-	Layers:
	-	`sha256:8fad4b39600d1cc9573d6e39a2a4edf5ad29cebd2dceccc170b1d725392b2147`  
		Last Modified: Fri, 12 Sep 2025 05:20:24 GMT  
		Size: 11.5 MB (11480759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87a347519f4556c4fd21062acb45a02e68300ee575174bcef5ea53271e062836`  
		Last Modified: Fri, 12 Sep 2025 05:20:24 GMT  
		Size: 25.9 KB (25911 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-21-and-24-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:570d4331d40ec7e1b075d74e9aead099ea74e34384b7ec0bc44610e640e3a81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.9 MB (614944748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2299287762610331a5bc204460d7b0f5fc9e4024c72af4a7539de3cade417886`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=21.0.8.9-1
# Thu, 17 Jul 2025 03:50:10 GMT
ARG package_version=1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:a2133584a03a0323a461f4ba1900a168268d3305d6206a4e0a210c92b146e94a`  
		Last Modified: Wed, 10 Sep 2025 02:34:05 GMT  
		Size: 52.8 MB (52775111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786316b8ae5b77f46f5dc354d692fb53f0aa9de45255ab4023dae3113e84466`  
		Last Modified: Fri, 12 Sep 2025 02:11:09 GMT  
		Size: 168.4 MB (168399303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bdf99aa12bbc5d915af6915f3bf6956462e2f923a7d8d5e2121e02f2703668`  
		Last Modified: Fri, 12 Sep 2025 14:51:14 GMT  
		Size: 171.2 MB (171230971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e608df7e9e464b559859c9e00152193ebb9952b54bf1752a8579117307bb8e6`  
		Last Modified: Fri, 12 Sep 2025 02:13:03 GMT  
		Size: 85.1 MB (85080713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de55da3725977d525ad16f57793059557b9c0752d4dfa4ef6720ca01fd407d`  
		Last Modified: Fri, 12 Sep 2025 02:12:54 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74a90fa5602429842e29463e846cf46d930c93c97ee8159446affd54bb5de3c`  
		Last Modified: Fri, 12 Sep 2025 14:49:21 GMT  
		Size: 137.5 MB (137456863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-21-and-24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5d0543d1321ebf6cd66fc5a86975373ed30bdc8c654b3ff7052fc8aa5ffbc501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11505336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8e22b93cfae713f4bf7c670f82703d915430ac8221f84b0fc7e8d96ca023da`

```dockerfile
```

-	Layers:
	-	`sha256:e5c19198e82371ece4afa616f77f01c9223b7bebd346bf5ca1646cce3364104b`  
		Last Modified: Fri, 12 Sep 2025 05:20:33 GMT  
		Size: 11.5 MB (11479169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea1cc38e01fbbb448956251b7c566267277def9ae498b16fe97c0642c93deac`  
		Last Modified: Fri, 12 Sep 2025 05:20:33 GMT  
		Size: 26.2 KB (26167 bytes)  
		MIME: application/vnd.in-toto+json
