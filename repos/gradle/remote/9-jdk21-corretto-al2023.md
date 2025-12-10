## `gradle:9-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:8e09dae2d930c3f390ebfa72e8cba032c9fdd7b1abc6100ea6358bf403eaf08a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:7aca105fef2e41f93757670d32b3f61a13fbe70bc73228b02f7e180a53c23450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.8 MB (445754613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5287832f7548037c59692cfabb34bbebcce70a0dfe32d7a9de0f51da6a4912d`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:25 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:24:25 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:24:25 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:24:25 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:11:57 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:11:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:11:57 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:11:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:11:58 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:11:58 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:11:58 GMT
ENV GRADLE_VERSION=9.2.1
# Wed, 03 Dec 2025 21:11:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Wed, 03 Dec 2025 21:12:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:12:00 GMT
USER gradle
# Wed, 03 Dec 2025 21:12:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 03 Dec 2025 21:12:00 GMT
USER root
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8cbd3c43733a7e197430ec594b9a379e73c2c0129499a285c897b482d00692`  
		Last Modified: Wed, 03 Dec 2025 21:11:35 GMT  
		Size: 170.2 MB (170185114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f08fff719a72c46ea57dd242fb7dcc76c50aad922e5b32e778feeb3c3355cf`  
		Last Modified: Wed, 03 Dec 2025 21:12:44 GMT  
		Size: 86.0 MB (86021931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f8e5217237c3ba2293e2cdf36c49f5cde29acac2eb5cbc09016d6d653c41a0`  
		Last Modified: Wed, 03 Dec 2025 21:12:38 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbda566b885e92e2e4aa61a82921c768b3c02e948fa8eccaf166c1c4d206414`  
		Last Modified: Thu, 04 Dec 2025 00:41:02 GMT  
		Size: 135.5 MB (135521966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e953ebb81cbcb97736f9e0086819bb95f6e3f820e78866bf89fb47efb4bbf24f`  
		Last Modified: Wed, 03 Dec 2025 21:12:38 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:cbb985f2e010d60a309e3ff873c4b5b98cffdac57f148bc9a960e64fa6eeb001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfb7e919c36764386e08219508a9eefe49b35e6a67fca73844d7df784ae7cc8`

```dockerfile
```

-	Layers:
	-	`sha256:d3db3a663e260bbeab468a517a9608dc3c76a759bcbc9aa925fa3dc9e4c18e0f`  
		Last Modified: Thu, 04 Dec 2025 00:23:45 GMT  
		Size: 11.3 MB (11337144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756009acfd853b593d6db5a2956bb0fb0014674e912cbedfae262509fb7aaf75`  
		Last Modified: Thu, 04 Dec 2025 00:23:46 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:346b22055a84b271b1eb884280718cece1c9a40b096ab4f01d707e2fa4a4157d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.4 MB (442422480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df65b1a66732d187935cdd10a121f47bcb02563770c7cc9a034399a9dfb0ff36`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:41 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:27:41 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:27:41 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:27:41 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 03 Dec 2025 21:11:23 GMT
CMD ["gradle"]
# Wed, 03 Dec 2025 21:11:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 03 Dec 2025 21:11:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 03 Dec 2025 21:11:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 03 Dec 2025 21:11:23 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 03 Dec 2025 21:11:23 GMT
WORKDIR /home/gradle
# Wed, 03 Dec 2025 21:11:23 GMT
ENV GRADLE_VERSION=9.2.1
# Wed, 03 Dec 2025 21:11:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Wed, 03 Dec 2025 21:11:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 03 Dec 2025 21:11:26 GMT
USER gradle
# Wed, 03 Dec 2025 21:11:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 03 Dec 2025 21:11:26 GMT
USER root
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626b53f4a673eb63ba52f6f5686c9b4a1a436ef18af99dc4556d8c58340ae1c5`  
		Last Modified: Wed, 03 Dec 2025 21:10:57 GMT  
		Size: 168.4 MB (168441796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3565fa216b9bed5b33ed82e13b6695f63272ae4e71a7405cb9be21b2cfaa3a98`  
		Last Modified: Wed, 03 Dec 2025 21:12:18 GMT  
		Size: 85.5 MB (85528081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8474b57afd6bb90456dc36df282c759160ac318f307e546b4618ee92b00b2b3b`  
		Last Modified: Wed, 03 Dec 2025 21:12:09 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb42ecac13fbcfef784085ba34549c49088697a5f0f0ff24cb3d0a29e01d5450`  
		Last Modified: Thu, 04 Dec 2025 10:19:52 GMT  
		Size: 135.5 MB (135521966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087c8652d00cbc6fd64a028d3b91084a01087fe5e3d70926e479e4880b7a8c02`  
		Last Modified: Wed, 03 Dec 2025 21:12:09 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:f0bd46ecd7ace2f69052d91bcdec938b2390a59f14a778676561428807bdf153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11357994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a05b8af51d0192030a897b9683b339b25f88e1316afd7aacdb6bba1a9b8028`

```dockerfile
```

-	Layers:
	-	`sha256:d8d970c5c05c8dedc477820ebbbaa6326f6131509d35f327839aa8aeb741aa70`  
		Last Modified: Thu, 04 Dec 2025 00:23:54 GMT  
		Size: 11.3 MB (11336146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1962f4289f1f7e696ab038ac43920f5ab1d6f902a57d65e41065ca3957493597`  
		Last Modified: Thu, 04 Dec 2025 00:23:54 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
