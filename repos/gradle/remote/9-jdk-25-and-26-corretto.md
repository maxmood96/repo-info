## `gradle:9-jdk-25-and-26-corretto`

```console
$ docker pull gradle@sha256:8a801faa956047756c185e11334e760188d2f53a6332a4e09c91b57b8670e78d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-26-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:23a075f27cf424439d91ab6d7b9dc3f9b73d1c5b5d5e442315fbb53d4a8cd4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **649.7 MB (649668303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51b6bf1bf8ebafdbb000a81c36d9f88ed2e016c055c0f400b3217a0f5d2d2f2`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:19:00 GMT
ARG version=25.0.3.9-1
# Sat, 09 May 2026 00:19:00 GMT
ARG package_version=1
# Sat, 09 May 2026 00:19:00 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:19:00 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:19:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 09 May 2026 01:20:32 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Sat, 09 May 2026 01:20:51 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 09 May 2026 01:20:51 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Sat, 09 May 2026 01:20:51 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:20:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:20:51 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:20:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 09 May 2026 01:20:51 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:20:51 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:20:51 GMT
ENV GRADLE_VERSION=9.5.0
# Sat, 09 May 2026 01:20:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Sat, 09 May 2026 01:20:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:20:54 GMT
USER gradle
# Sat, 09 May 2026 01:20:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:20:54 GMT
USER root
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0250ec3d728132a010a8ee425e754a8d5a13a96838c49f810421351398ab603e`  
		Last Modified: Sat, 09 May 2026 00:19:24 GMT  
		Size: 189.4 MB (189411044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926cd012f5d91dc89d948ae3081d8d87c97e5000c1823f9242413a251f73d0e6`  
		Last Modified: Sat, 09 May 2026 01:21:33 GMT  
		Size: 179.2 MB (179247368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fa3e1d4553c41efc18d2385b751efb76a2c53c6641e35b068ddcf6ee2b970e`  
		Last Modified: Sat, 09 May 2026 01:21:31 GMT  
		Size: 86.2 MB (86169750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ccb976ea027074bfed8232d9f6923a84f47c6b5f2e3f981798ced15060fa30`  
		Last Modified: Sat, 09 May 2026 01:21:26 GMT  
		Size: 1.8 KB (1757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06d2dc8d70080034d49a981b8261dcd5e0c67ae4273390ceac52aaf71a3ab5b`  
		Last Modified: Sat, 09 May 2026 01:21:33 GMT  
		Size: 140.2 MB (140235943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9416ca578760977985ced2a5f75cfd58deae77e6db62e1850473fc64a4d82a16`  
		Last Modified: Sat, 09 May 2026 01:21:27 GMT  
		Size: 25.6 KB (25605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:28d07ccaba7804c29388508edaeb9196ee0f40158772f6f5c51989f30c7fd489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11574153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b331f5a695914d4aa609d538c329fa9c113e9cdc3e663c80fff6ddde3b238e9a`

```dockerfile
```

-	Layers:
	-	`sha256:30e9956f49f949fa9993034ccbe4c9e5ee20b39f79ea94150a6cb18154d8fad5`  
		Last Modified: Sat, 09 May 2026 01:21:27 GMT  
		Size: 11.5 MB (11544643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17b9b1d65874d80844b02c0602f558c5c6d5f8cfc27dcbecfe53a57c03b287cf`  
		Last Modified: Sat, 09 May 2026 01:21:26 GMT  
		Size: 29.5 KB (29510 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-26-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:53cb24a9d3f6c74847f5178cf780c07769be667a4715f32b13c265779c3890c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.8 MB (643837771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ce3880b522c1253e4e4ebee76df2b2de7be9a769b7eb19a015d36fbb4dd2e9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:48 GMT
ARG version=25.0.3.9-1
# Sat, 09 May 2026 00:16:48 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:48 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:48 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 09 May 2026 01:45:38 GMT
COPY /usr/lib/jvm/java-26-amazon-corretto /usr/lib/jvm/java-26-amazon-corretto # buildkit
# Sat, 09 May 2026 01:46:00 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 09 May 2026 01:46:00 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Sat, 09 May 2026 01:46:00 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:46:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:46:00 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:46:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 09 May 2026 01:46:00 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:46:00 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:46:00 GMT
ENV GRADLE_VERSION=9.5.0
# Sat, 09 May 2026 01:46:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Sat, 09 May 2026 01:46:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:46:03 GMT
USER gradle
# Sat, 09 May 2026 01:46:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:46:04 GMT
USER root
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650af40d683d967f6be2238c5da49e6232e999e2dbcf6f6803931dde1fea81a8`  
		Last Modified: Sat, 09 May 2026 00:17:16 GMT  
		Size: 187.3 MB (187330634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4cc446d7dc09584d9d6fbdb17f7269ef6a96bbad8d27a8f54e372900a33bde`  
		Last Modified: Sat, 09 May 2026 01:46:44 GMT  
		Size: 177.1 MB (177119391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19adc3bff3a68022c7f3892c8e9cd00a1b1efa985bd680b67a4193602c3872a3`  
		Last Modified: Sat, 09 May 2026 01:46:42 GMT  
		Size: 85.7 MB (85663709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c03b67ef57d29528b574fcbdbeeeb415a17e0f22e252e6cb93b0c9cc16680da`  
		Last Modified: Sat, 09 May 2026 01:46:35 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971eadf121d5913a297c212cd42ec571f5e3802836bb4483e415c5369a5f2776`  
		Last Modified: Sat, 09 May 2026 01:46:43 GMT  
		Size: 140.2 MB (140235939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596e6c10666298322904ea503648ec6f82ee295f5fdbe90481032849a4e5b516`  
		Last Modified: Sat, 09 May 2026 01:46:37 GMT  
		Size: 29.3 KB (29333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:75fbdfa7ce57411b39189ce6c95f4a623351bdfa3873b80eab45f25884908201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11572942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9766d701bde06b0524606cd894de35955c424226b826378b0b00a3b91d3ddb`

```dockerfile
```

-	Layers:
	-	`sha256:69c739307841533da3e9a852a4cef89e73869287bf9ececfce9c56f658b878b7`  
		Last Modified: Sat, 09 May 2026 01:46:37 GMT  
		Size: 11.5 MB (11543113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f332fbf545b73d871d88dcbc1969684f80897dd849fe226eaec476d08a4c4e8a`  
		Last Modified: Sat, 09 May 2026 01:46:35 GMT  
		Size: 29.8 KB (29829 bytes)  
		MIME: application/vnd.in-toto+json
