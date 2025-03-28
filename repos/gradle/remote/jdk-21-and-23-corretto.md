## `gradle:jdk-21-and-23-corretto`

```console
$ docker pull gradle@sha256:609bc3eda3330acf91b72612f16e96c96f99c1895448b9f8f8212d3a36901171
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-23-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:73d83decc3c24edc79620c214aeaf1046fd846b486f830a041d7f1c29e4d270e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.7 MB (595661417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc96cf54e35432f04b59a2b3c220ed05e859ef1c774f24615d36a6f3624ae01b`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:27 GMT
COPY /rootfs/ / # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:27 GMT
ARG version=21.0.6.7-1
# Tue, 04 Mar 2025 19:20:27 GMT
ARG package_version=1
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956b70775b1a3090c93410d5b7322deac146fde209a8a0f3c1b55473fe670dd0`  
		Last Modified: Thu, 27 Mar 2025 23:58:52 GMT  
		Size: 169.8 MB (169756668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad161a3f58858f5f7fe3111ea16a4a0e55386e1f8c315b4c7cafe57145abb1e6`  
		Last Modified: Fri, 28 Mar 2025 00:08:51 GMT  
		Size: 163.5 MB (163481782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d5c005d93a85999e4b25890939ab40b4bb5bf353a66368f85e80113c107e41`  
		Last Modified: Fri, 28 Mar 2025 00:08:49 GMT  
		Size: 72.3 MB (72257222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e857bee53646a2ebfd865b2c0d02d3fb7cc29a7c2b488130f9a02f10d8bbb8`  
		Last Modified: Fri, 28 Mar 2025 00:08:46 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3052ff40c0e118a44ddae34060183e4a584a72cbbd582f23e4dae25d302da65`  
		Last Modified: Fri, 28 Mar 2025 00:08:51 GMT  
		Size: 137.0 MB (137040670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b943ec2ff7e32d409e446736e2f7be7d00bb7e9ff2d8aea423bd61e900c22791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10928917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2677ba8f7cbcb86ec396cef3fba8a76c65c7dc0a8eafef8c3d0700d738e9ae96`

```dockerfile
```

-	Layers:
	-	`sha256:5e7a1cffa17ac1e3d52d18384549473eb861ffed44c16079d0125e56930df2ea`  
		Last Modified: Fri, 28 Mar 2025 00:08:47 GMT  
		Size: 10.9 MB (10903281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3c5eb4e6133312ab6a19a67f6aca137e6b9c8de9d48d416d3c1d5e4fdd2035`  
		Last Modified: Fri, 28 Mar 2025 00:08:46 GMT  
		Size: 25.6 KB (25636 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-23-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:25c8b54ded47ccb1603df9f11ad9308a696aed641ddc71ad441bcd6d355e6f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.9 MB (590874815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10481f1630ebedcec5daa174f395cf5c6b338b69ec081bf2ff512bf518ca18a2`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 04 Mar 2025 19:20:27 GMT
COPY /rootfs/ / # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["/bin/bash"]
# Tue, 04 Mar 2025 19:20:27 GMT
ARG version=21.0.6.7-1
# Tue, 04 Mar 2025 19:20:27 GMT
ARG package_version=1
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV LANG=C.UTF-8
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 04 Mar 2025 19:20:27 GMT
CMD ["gradle"]
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 04 Mar 2025 19:20:27 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Mar 2025 19:20:27 GMT
WORKDIR /home/gradle
# Tue, 04 Mar 2025 19:20:27 GMT
ENV GRADLE_VERSION=8.13
# Tue, 04 Mar 2025 19:20:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Tue, 04 Mar 2025 19:20:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:92a376874570d50aaa72a4435a5b15fdfcdc3099600b45751b2c0705bd2c65f2`  
		Last Modified: Thu, 27 Mar 2025 02:43:04 GMT  
		Size: 52.2 MB (52247990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a55f16bfd894345fc4cb8cbd646e1de4efd1f812d559fc8f061f8e83f825c82`  
		Last Modified: Fri, 28 Mar 2025 00:20:31 GMT  
		Size: 168.1 MB (168069708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965448f46dab3e5be6981298507cd0be91cfdbca2eccf49a8b2c737ea3feed89`  
		Last Modified: Fri, 28 Mar 2025 01:20:21 GMT  
		Size: 161.6 MB (161571430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e828595ffea0e1d3d78cd861172c081f9efd1fa88eadc3e5cbb74551f0dd0863`  
		Last Modified: Fri, 28 Mar 2025 01:20:20 GMT  
		Size: 71.9 MB (71933213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a83da22f050b90135f31eda46754dc8fcf06f3441a7fbcec761e12fa50ce56`  
		Last Modified: Fri, 28 Mar 2025 01:20:17 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff905598d08412e8a77be477615b5a740aaad1fa60031371fd22b9743f8bf8`  
		Last Modified: Fri, 28 Mar 2025 01:20:21 GMT  
		Size: 137.1 MB (137050686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7df3e52fbd3e4e14e0a35a4fb0788adf954186d4b8956880ca52db7b5b5c93d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10927042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85db3c8887afa509d98cdd0d78aecb32e3954bf00a2c5a230311678bc09fa69e`

```dockerfile
```

-	Layers:
	-	`sha256:040e7306252e2d6af47c95c0f134cf07260c9b4965c2345a8044ac49a09c6d34`  
		Last Modified: Fri, 28 Mar 2025 01:20:18 GMT  
		Size: 10.9 MB (10901102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03f4e74c9bff10f5f5f92e13d2c84e7ab6c370cd8e8913215c2b5ec5774316c`  
		Last Modified: Fri, 28 Mar 2025 01:20:17 GMT  
		Size: 25.9 KB (25940 bytes)  
		MIME: application/vnd.in-toto+json
