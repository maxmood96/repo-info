## `gradle:9-jdk-25-and-25-corretto-al2023`

```console
$ docker pull gradle@sha256:869cc769cae3e7738f2b556bc73bf183aa200c340f7dc57bb517ffb7cfd436ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-25-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:0e890c1b102425b53716c36745f17dab81159bb97ecb97706beb190ae19f8fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.4 MB (464357999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b51f591e987bfc540cc68e2800452346268172f1b327b7fd42456c290e1f4e0`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:37 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 23:12:37 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:37 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:37 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 07 Nov 2025 00:12:07 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 07 Nov 2025 00:12:07 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 07 Nov 2025 00:12:07 GMT
CMD ["gradle"]
# Fri, 07 Nov 2025 00:12:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 07 Nov 2025 00:12:07 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 07 Nov 2025 00:12:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 07 Nov 2025 00:12:07 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 07 Nov 2025 00:12:07 GMT
WORKDIR /home/gradle
# Fri, 07 Nov 2025 00:12:07 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 07 Nov 2025 00:12:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 07 Nov 2025 00:12:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ff4d7205da8b8271c826b4d33c535dc537a1d647dc5aaac7acbed9389cdd36`  
		Last Modified: Fri, 07 Nov 2025 00:11:33 GMT  
		Size: 189.2 MB (189168050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968ba045b139035a87383c10499126c2ec553f7157ce8a2ac5481076db4c7ee`  
		Last Modified: Fri, 07 Nov 2025 00:12:59 GMT  
		Size: 85.6 MB (85613063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c20d78c99ee955afcea749cd0bbff4b43b0b16d9aa8edaa5fc24eafa11ef8`  
		Last Modified: Fri, 07 Nov 2025 00:12:51 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83d5f2aa449c03b6ab348238a2106a3a92df9d9d30ad8968ec25f84378e76d19`  
		Last Modified: Fri, 07 Nov 2025 06:20:23 GMT  
		Size: 135.6 MB (135574592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:335a41bcf3e89513b1eba1ae2eff3d6e1b629e9b8adff54c1e0653d17172dbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11354742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e27b30c7b402d585696b2f3d78b12189515b07c936ca32a2127b91d4780b9c`

```dockerfile
```

-	Layers:
	-	`sha256:c2a4a6cc757a3df13ac7ab4c815f5a2c365eb7780b3616bf9c5d33d908983cb5`  
		Last Modified: Fri, 07 Nov 2025 03:22:46 GMT  
		Size: 11.3 MB (11330303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d95bd8be7bc8d7ccff496744c284500f17b2fb3b83950c0c3f35d41eb258c66`  
		Last Modified: Fri, 07 Nov 2025 03:22:47 GMT  
		Size: 24.4 KB (24439 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-25-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:10019741cb6e33f3a9956cb976359f31a7e907d37a98d12809761186850c18ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.7 MB (460743204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6de94d652728a3cc84d6b9ea69ba8e11d77e57db1fa31bd7adefcfbabed2d28f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:39 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 22:14:39 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:14:39 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:14:39 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 06 Nov 2025 23:11:52 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 06 Nov 2025 23:11:52 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 06 Nov 2025 23:11:52 GMT
CMD ["gradle"]
# Thu, 06 Nov 2025 23:11:52 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Nov 2025 23:11:52 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Nov 2025 23:11:52 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 06 Nov 2025 23:11:52 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Nov 2025 23:11:52 GMT
WORKDIR /home/gradle
# Thu, 06 Nov 2025 23:11:52 GMT
ENV GRADLE_VERSION=9.2.0
# Thu, 06 Nov 2025 23:11:52 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Thu, 06 Nov 2025 23:11:55 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123460810639ecd99796c2d04c9c602287fe1bbb2613c2622aabd5176f1a2c40`  
		Last Modified: Thu, 06 Nov 2025 23:10:36 GMT  
		Size: 187.1 MB (187092407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2282b433126351253f759c3e5bb514e20b04b9d322a2d276a1081eb17cd38379`  
		Last Modified: Thu, 06 Nov 2025 23:13:01 GMT  
		Size: 85.2 MB (85165580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f322fa2aa266714627c37870c26b61b3f81fb135377545947c64d092a88e076`  
		Last Modified: Thu, 06 Nov 2025 23:12:48 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec392eae36957f1f103e2f91a39460915ca4c0986d346271b60fbc684dce9a7`  
		Last Modified: Fri, 07 Nov 2025 14:46:15 GMT  
		Size: 135.6 MB (135581742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:aecf620a7de8a372974c6df9387d5578a9285ed37219cdd68e40437afcca0a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11354128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce10b3cb5c2545a749e3844f6be96d4035f75255af80a68b7b08d316577a6f0`

```dockerfile
```

-	Layers:
	-	`sha256:aa642165530087e0e33889cfd27de9a63d9c0bbbc41372f7a269812fd382c1c7`  
		Last Modified: Fri, 07 Nov 2025 00:22:47 GMT  
		Size: 11.3 MB (11329412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9e37bf2d06a9a4e0ab45a0ed5dd5b80ec77a2fc3d150050243ae8f82930c27`  
		Last Modified: Fri, 07 Nov 2025 00:22:48 GMT  
		Size: 24.7 KB (24716 bytes)  
		MIME: application/vnd.in-toto+json
