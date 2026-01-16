## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:54bf502ce9fb73162aca8fa285421c30de6f3c6977ff00271fdef99f9872095c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:f28c1655374800bba3365bcea8471eba02f7ab950fbc15d42ff08f9425b3719e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.6 MB (447646520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68fded0ff12d0b6d773cb31b72369496ba374b1b7e29cc8caf7c7c11594c51`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:40 GMT
ARG version=21.0.9.11-1
# Thu, 18 Dec 2025 01:18:40 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:18:40 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:18:40 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 18 Dec 2025 02:18:56 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:18:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:18:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:18:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:18:57 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:18:57 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:18:57 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 18 Dec 2025 02:18:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 18 Dec 2025 02:18:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:18:59 GMT
USER gradle
# Thu, 18 Dec 2025 02:18:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:18:59 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6113d4b7ab7a5acb2f4b4897a2154fedabeed4d6662b5afd47f2928b0778326c`  
		Last Modified: Thu, 18 Dec 2025 01:19:27 GMT  
		Size: 170.2 MB (170185789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f8ddc83f24b99fac07d362aa075bc9096c20221ec223bc4e2c85348d6b6e12`  
		Last Modified: Thu, 18 Dec 2025 02:19:47 GMT  
		Size: 86.0 MB (86020495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0233aa05e1bc12cff3808bd1a5019bd77b2ec5f562511d5c1ee34f12612d2c3`  
		Last Modified: Thu, 18 Dec 2025 02:19:39 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1335c7bdcbcf4ed5879d553c7bff9bfec64c6bb28cc526f8165157a3a4deac3`  
		Last Modified: Thu, 18 Dec 2025 02:20:09 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a83d91774852ead06e7a928e811e0f54c41dad64b3f74f2c7a4566c5397ba5f`  
		Last Modified: Thu, 18 Dec 2025 02:19:39 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:e268999278ddedbdce33b7af3a4d0ea12143ef8cc0ca605f9bfbdb1e5d4f4897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f876798b304cea567d45a4f4c36d063f1b804371d6a1679e066f0b0f1f8326d`

```dockerfile
```

-	Layers:
	-	`sha256:38d856e54e65779ecf73d1cd2b064905b7a7eadbec82b1b4806fd63364f2cff3`  
		Last Modified: Thu, 18 Dec 2025 03:20:06 GMT  
		Size: 11.3 MB (11342268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe6c6f298bb37a1d6eefa871010f2cd44b24795fe4d3f3d308d773497594a55`  
		Last Modified: Thu, 18 Dec 2025 03:20:08 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d40677437c95a146db8a37ff1cb0dc3bc37e180a0aed042818cdae087591d54f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444330434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c634a62fe8d5e18193b814c1ff3e091732388ce19fe3dc748ab3926a32da703e`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:40 GMT
ARG version=21.0.9.11-1
# Thu, 15 Jan 2026 22:09:40 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:09:40 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:09:40 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 15 Jan 2026 23:15:02 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 23:15:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 23:15:02 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 23:15:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 23:15:02 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 23:15:02 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 23:15:02 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 15 Jan 2026 23:15:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 15 Jan 2026 23:15:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 23:15:05 GMT
USER gradle
# Thu, 15 Jan 2026 23:15:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 23:15:05 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebe1c9b0f4ea4f18ee5432a1b5928f5a2edd15a835cff3cbdf602ca3e6f769e`  
		Last Modified: Thu, 15 Jan 2026 22:10:20 GMT  
		Size: 168.4 MB (168441565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f978441bcfb26ae1b193eef3587b7529e71ee35d49c56a642b4aaa03ec232a1c`  
		Last Modified: Thu, 15 Jan 2026 23:15:53 GMT  
		Size: 85.5 MB (85518107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1eb94f0b45f5a4164cede73f4aecc850700095bb4e1d7735fb14f223b5cf61`  
		Last Modified: Thu, 15 Jan 2026 23:15:45 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c77852ff439668b8e36727e20cdc705b68d90948798a1900b9e4100635acf9`  
		Last Modified: Thu, 15 Jan 2026 23:15:55 GMT  
		Size: 137.4 MB (137395197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3462eb6460569052c8fc841c9d9ea7dc4a4d3e41aac475d05e1de7ce3c7296`  
		Last Modified: Thu, 15 Jan 2026 23:15:46 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:04ccd320fc01f7ac065a71bcd95305738d8645b91ebbb33a8127b6420e6b777d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11362304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefd24604d287fda9c7456ac100e4caa34482ea53851b514234e579c24805b78`

```dockerfile
```

-	Layers:
	-	`sha256:c98e98dd51a06d2374fb19e618b6f28639c61626aa70bdea06238636e7353000`  
		Last Modified: Fri, 16 Jan 2026 00:27:52 GMT  
		Size: 11.3 MB (11341250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f9542c793fc54e80f5155fda24d5c168968fa30749b9cdda69ccbeabcf93c6f`  
		Last Modified: Fri, 16 Jan 2026 00:27:53 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
