## `gradle:9-jdk-lts-and-current-corretto`

```console
$ docker pull gradle@sha256:1d2c933457267216510c7af783d20f9de6fd3101e4ee66c9604947ec31a72847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-lts-and-current-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:64cf29381b44b090f02b90de3876c4d4bc96f3d2c9d82b5d548cc15fa61d9257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.3 MB (463277643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a52068e9f95bbf362d1ec0b939d3a24c6c655885e13176cf188732ff38e2074`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 30 Sep 2025 09:31:25 GMT
CMD ["gradle"]
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 30 Sep 2025 09:31:25 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 30 Sep 2025 09:31:25 GMT
WORKDIR /home/gradle
# Tue, 30 Sep 2025 09:31:25 GMT
ENV GRADLE_VERSION=9.1.0
# Tue, 30 Sep 2025 09:31:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Tue, 30 Sep 2025 09:31:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a075fb8961d282a9f92fb75aaa159d8011cb3dba1aa6fea626361cc411336906`  
		Last Modified: Thu, 25 Sep 2025 03:19:01 GMT  
		Size: 189.1 MB (189134365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39d11c8385bc2d739c9ccd96663f3a7efb2f145a987e9c8e81f77dd77437b05`  
		Last Modified: Wed, 01 Oct 2025 13:24:36 GMT  
		Size: 85.6 MB (85563447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa90225252e88a1cc62d0e54249cf0f208b9f1ca3ea97f3ae54b65d6bab540b`  
		Last Modified: Tue, 30 Sep 2025 17:50:42 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50230c30ab1d20c1556442e43eda61fa42d9dabe38c4c2b5be1ff1b124e3a305`  
		Last Modified: Wed, 01 Oct 2025 13:24:35 GMT  
		Size: 134.6 MB (134572758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0244c9516ecadba369f5d17ea716ffa6e08ae43f41af4cd0b5dc5163e82f46bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11341023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498976587234ef3589beac73b4612f27be782bfec213e385731a653c076b0c8c`

```dockerfile
```

-	Layers:
	-	`sha256:e43309f6e548b540cb65692113c735fc081e1b80bfd1b04c04dc7262dd7f657e`  
		Last Modified: Wed, 01 Oct 2025 14:21:19 GMT  
		Size: 11.3 MB (11316541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16a8ec26c9583479137e8f2b652af0904b5697ae8f2b881df560682468e209b5`  
		Last Modified: Wed, 01 Oct 2025 14:21:20 GMT  
		Size: 24.5 KB (24482 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-lts-and-current-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b1e38ec0682676d5e982ec0da4aab7d0669f9b4274010ca038307cda7e3cb72f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612193935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a4ae2618e3a5a6403d239680097a016e7edd0a878c97465806b5cb11417562`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 19 Sep 2025 14:40:42 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 19 Sep 2025 14:40:42 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Fri, 19 Sep 2025 14:40:42 GMT
CMD ["gradle"]
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 19 Sep 2025 14:40:42 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 19 Sep 2025 14:40:42 GMT
WORKDIR /home/gradle
# Fri, 19 Sep 2025 14:40:42 GMT
ENV GRADLE_VERSION=9.1.0
# Fri, 19 Sep 2025 14:40:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
# Fri, 19 Sep 2025 14:40:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=a17ddd85a26b6a7f5ddb71ff8b05fc5104c0202c6e64782429790c933686c806
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda7a391125898fe088b7a329ba667267f6a8e4cd156d822b71c3cc24d07388e`  
		Last Modified: Wed, 24 Sep 2025 22:10:27 GMT  
		Size: 168.4 MB (168400554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0a9085c5e5b09821622a8b30a93c409ac471dd7045d78b3cbbb631bd2d47e4`  
		Last Modified: Thu, 25 Sep 2025 20:06:59 GMT  
		Size: 171.2 MB (171230936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6aa2011b49ffec428a7990c01a4dcb6e729c3fae1d3dbb18c99fdbd059ace2`  
		Last Modified: Wed, 24 Sep 2025 22:13:06 GMT  
		Size: 85.1 MB (85083620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b6200ae0696296a9d7fad079eb7c7f159b743af25c01240b48a0cd4713752e`  
		Last Modified: Wed, 24 Sep 2025 22:12:57 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23a8dc94a646ec64eeb85e12d12005e7af6c04855c25a37d73b7ae4218ddd06`  
		Last Modified: Thu, 25 Sep 2025 10:00:29 GMT  
		Size: 134.6 MB (134577596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-lts-and-current-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:d21d999969c082ad709397313bcbe1d39cbc72e8ea7e41776ba51f76f1c88878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11495595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d686eefd4008cfb9fbfbc3267b5a3d8f4e9870f73fe69f9f3b449826b9f11ff6`

```dockerfile
```

-	Layers:
	-	`sha256:35874af9a3faab03208a238f6c6ea86142c37cc382c3909121fd8abbca1d03a8`  
		Last Modified: Thu, 25 Sep 2025 02:23:44 GMT  
		Size: 11.5 MB (11468026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931d534dcff852875c4cfc74a74e7af928f334993cc9874896e6c1c54ff5790a`  
		Last Modified: Thu, 25 Sep 2025 02:23:45 GMT  
		Size: 27.6 KB (27569 bytes)  
		MIME: application/vnd.in-toto+json
