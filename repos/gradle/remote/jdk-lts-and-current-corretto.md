## `gradle:jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:d20d64d8f32ba8f95a4af5e50f7fb41ef9f1cb20494c76ac69ae13421ea7a487
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:b1011e90b5e5b2fb3bf445e8a5fac639ae1781b118046a554052977a513c3d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.4 MB (464356184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38e8a0aa490f6cafde7599d9e4c6ef5b04bb2f1a3a5675f7ce23280a408c22`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:49 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:12:49 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:49 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:49 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:11:30 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:11:30 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:11:30 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:11:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:11:30 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:11:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 31 Oct 2025 01:11:30 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:11:30 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:11:30 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 31 Oct 2025 01:11:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 31 Oct 2025 01:11:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cad330e08d585bcff7ce7b398a5a2dbb684e338ae4fe298f9dca43f057f4b8c`  
		Last Modified: Fri, 31 Oct 2025 01:10:53 GMT  
		Size: 189.2 MB (189165602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230e862c5281f22f664b7a1113d0b517bf4bb3fdc55d83e76bcc7b13158ee2ea`  
		Last Modified: Fri, 31 Oct 2025 01:12:17 GMT  
		Size: 85.6 MB (85613005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb20f863c5e3f2fb3104e62374fdc0f66fcc25cb5f07fc2cf0aaa57d904bbb8`  
		Last Modified: Fri, 31 Oct 2025 01:12:09 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166abdb79215b3e5a62b645dd0bb31fca7340ee7a3f4011de09893b4c9ef384e`  
		Last Modified: Fri, 31 Oct 2025 04:46:44 GMT  
		Size: 135.6 MB (135574554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:03d78c1cce22888c4b3897c8cd5591712dd894d5d5919ee6c0ad92056316521c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11354742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee494611d063f3fee4747a083e003a3f83317aabae3e7250edcc005aa139dcea`

```dockerfile
```

-	Layers:
	-	`sha256:b2e81b259e9f80c9727b2c65789a26845bd112c1b3aa5fe5031022281d711b4e`  
		Last Modified: Fri, 31 Oct 2025 02:22:53 GMT  
		Size: 11.3 MB (11330303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:302c4e2cb57f1b61ddcde3186f45512dd91c84434a3c6cccdea3bd6c3c19f89a`  
		Last Modified: Fri, 31 Oct 2025 02:22:54 GMT  
		Size: 24.4 KB (24439 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2c57a3723f8c51d53b2e90d16db147ab3dbb780c4a9f1ec3109a3c91ea9b3571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.7 MB (460740710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d20a9e746cb1e26cecc4cb04b06314862b19b4d341a0d830de636ea1237d1a0`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:13:18 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:13:18 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:13:18 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:13:18 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:13:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:11:55 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:11:55 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:11:55 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:11:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:11:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:11:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 31 Oct 2025 01:11:56 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:11:56 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:11:56 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 31 Oct 2025 01:11:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 31 Oct 2025 01:11:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57b7d335691ba03f63339309551160b358c13633bf8b3ed736c5fb71399b7e5`  
		Last Modified: Fri, 31 Oct 2025 01:11:07 GMT  
		Size: 187.1 MB (187089365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c4bad7899e064b8d6c82fc3d2c04bc42674acdc245d93df8a39ab0735a0790`  
		Last Modified: Fri, 31 Oct 2025 01:12:45 GMT  
		Size: 85.2 MB (85165867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843df8df2ebd6b49577c1b30ecaf9da699627f640d14ebe630938a67e632fd5`  
		Last Modified: Fri, 31 Oct 2025 01:12:36 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69594450168932282b1b8ae53020688fb4fc23f550430b410b677a20e4059de`  
		Last Modified: Fri, 31 Oct 2025 01:12:33 GMT  
		Size: 135.6 MB (135581837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:f7f65acffa68ec93e826be1b2995ce2888e23b4149af1ae6a084e103378dc3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11354129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9cb8c9697e986917220f5bcaa869879834305c004f910a8f63ff3f937c6566`

```dockerfile
```

-	Layers:
	-	`sha256:1eb067fd773bfc12569ef15be921d0bb72620d79e2994c8475b27a8b70e6ae02`  
		Last Modified: Fri, 31 Oct 2025 02:23:03 GMT  
		Size: 11.3 MB (11329412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369fc75106afd9ee734cb8a3a7856740cb4f38784082448a881976257b679224`  
		Last Modified: Fri, 31 Oct 2025 02:23:04 GMT  
		Size: 24.7 KB (24717 bytes)  
		MIME: application/vnd.in-toto+json
