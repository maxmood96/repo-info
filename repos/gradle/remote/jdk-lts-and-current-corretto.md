## `gradle:jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:26578d9617ba64b7b4b6c3afc714e1cac34b4c5917ee5db8759e0a647de88f21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:2ebeed5d845aaa9e6cf9c96155128adba95de2ef25f100a4984177aba61b6523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.3 MB (466265680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c670c0e71d356aca692a42c1fc204c3c1f3c97be9db284d2959954d853ee6a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:01:49 GMT
ARG version=25.0.2.10-1
# Wed, 21 Jan 2026 19:01:49 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:01:49 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:01:49 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 21 Jan 2026 19:15:03 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 21 Jan 2026 19:15:03 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 21 Jan 2026 19:15:03 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:15:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:15:03 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:15:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 21 Jan 2026 19:15:03 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:15:03 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:15:03 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 21 Jan 2026 19:15:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 21 Jan 2026 19:15:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:15:05 GMT
USER gradle
# Wed, 21 Jan 2026 19:15:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 21 Jan 2026 19:15:06 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84184861cf3f73b067f6e2b91043dbc78ff544f7b571af6af75864a9e885dba`  
		Last Modified: Wed, 21 Jan 2026 19:02:14 GMT  
		Size: 189.2 MB (189191314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ead61e2cbaf6d884ae85902806006433b141413fabd3262ec740170bb379a`  
		Last Modified: Wed, 21 Jan 2026 19:15:31 GMT  
		Size: 86.0 MB (86036915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54179a08442ed94f255390125feb2581761f6ee4ddbb504e4762e6f4506ec78`  
		Last Modified: Wed, 21 Jan 2026 19:15:28 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45599c8366650f64a0f782e494f699573acc479ec4f4e99d725f22756fdac135`  
		Last Modified: Wed, 21 Jan 2026 19:15:32 GMT  
		Size: 137.0 MB (136988866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f6d51ac0ed37b5bc8275fbaa2499d4c9695d5cd346c6ee20d792b54de2cdd2`  
		Last Modified: Wed, 21 Jan 2026 19:15:28 GMT  
		Size: 25.6 KB (25594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a65968a96701e014bf06fac897673d0e890a08feddc6829c9f7dc0558e7bd1d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11367138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cfaa311571dfed11fc532aab526b6024102da379a179c9d9c187f720dfd69f`

```dockerfile
```

-	Layers:
	-	`sha256:d545106423733c0142c5cf0e28e5960b66029d7564d03752ff0195c0311804b6`  
		Last Modified: Wed, 21 Jan 2026 19:15:29 GMT  
		Size: 11.3 MB (11340661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e080f6d8eb139b8a7ca5ff14c6367816d5238b6cfa39e6e326ef349a62e7c8`  
		Last Modified: Wed, 21 Jan 2026 19:15:28 GMT  
		Size: 26.5 KB (26477 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2af58937abb5f0052a697a48b8f5ef26834cba23f1221fc6d771a082e8235d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.5 MB (462541849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfab27c838989231744e31be39c3c8142e1b8a376962740f4ebd843d7964bf3`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:02:03 GMT
ARG version=25.0.2.10-1
# Wed, 21 Jan 2026 19:02:03 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:02:03 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:02:03 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:02:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 21 Jan 2026 19:17:03 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 21 Jan 2026 19:17:03 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 21 Jan 2026 19:17:03 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:17:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:17:03 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:17:03 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Wed, 21 Jan 2026 19:17:03 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:17:03 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:17:03 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 21 Jan 2026 19:17:03 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 21 Jan 2026 19:17:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:17:05 GMT
USER gradle
# Wed, 21 Jan 2026 19:17:06 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 21 Jan 2026 19:17:06 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1219b2dc527a7d7920fc18d43a9d921a6ec165aad6ec37677541ec00415a03`  
		Last Modified: Wed, 21 Jan 2026 19:02:28 GMT  
		Size: 187.1 MB (187090489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c118a2af44b21a3c0021a10df48b935f744d1154c19bacb51ee0847be44c47`  
		Last Modified: Wed, 21 Jan 2026 19:17:38 GMT  
		Size: 85.5 MB (85517028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b9357b2901453430e37b37bfd9808bfc72b39503c3fe11bcc9bd10626c894d`  
		Last Modified: Wed, 21 Jan 2026 19:17:34 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e9b1c5937f6c1d45e13feb771e923eebe5140ecdd4f440e24ded7a65b02059`  
		Last Modified: Wed, 21 Jan 2026 19:17:39 GMT  
		Size: 137.0 MB (136988868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb77686acf8a48463abfe24034dd5635d5f94b05ac59d3842a0657438fc1fae`  
		Last Modified: Wed, 21 Jan 2026 19:17:34 GMT  
		Size: 29.3 KB (29317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c606f32c31089407f8b5fac88892eaae0680f4672c834a1042116820d4bc64b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11366540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8932660b2853fe069492e8a552b7111f8096aa74d997e9eb4915fbc9c81664f8`

```dockerfile
```

-	Layers:
	-	`sha256:9f69d167218ce6b19ecddc4fe560f5c902a2ddf73efbca60e3c4e9ddd2f894a9`  
		Last Modified: Wed, 21 Jan 2026 19:17:35 GMT  
		Size: 11.3 MB (11339770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:574b8e700faad6d8572d1a0bd1711ea528448a873545ee7ad421b3ca5ae6e639`  
		Last Modified: Wed, 21 Jan 2026 19:17:34 GMT  
		Size: 26.8 KB (26770 bytes)  
		MIME: application/vnd.in-toto+json
