## `gradle:8-jdk21-corretto`

```console
$ docker pull gradle@sha256:bd328191a82e5d0840b80376ed9a2e7ed6c6bdcd8d84a32ead67452acd2a48ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:079e7bb8d6591188cf3d7470678a268d01c9677efc3d7fa3c2c0ed3eecdc79a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.3 MB (448307977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0da9ad1e7d60c7294ceebc9c39df5652fc31d090eea80a37acdcc8baf516730`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:54 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 22:14:54 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:54 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:54 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 23:12:01 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:01 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:01 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:01 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 23:12:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 23:12:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:03 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:04 GMT
USER root
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a008dca2fff34c89bb6e272e0474289359dfc4286d48d849d77b48a8f3db335`  
		Last Modified: Fri, 03 Apr 2026 22:15:19 GMT  
		Size: 170.2 MB (170194101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243a364ce2635470bf7d1e376bdc9fda9a3800484a69569ef0e76b8e1cc1d416`  
		Last Modified: Fri, 03 Apr 2026 23:12:36 GMT  
		Size: 86.1 MB (86097693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9692ba84c72912dbf3fc177d0a48b7abfbfc5fbad8d95fa48bc63db9b8a6d445`  
		Last Modified: Fri, 03 Apr 2026 23:12:32 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ed4959961dba695faeeb34138292703a765fbe96ff6b355c7bba065399403`  
		Last Modified: Fri, 03 Apr 2026 23:12:37 GMT  
		Size: 137.4 MB (137388294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4136ae85043841daa760ee780e1e7749a4d00aff411c4e26df5ddef4dd8f69e7`  
		Last Modified: Fri, 03 Apr 2026 23:12:32 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bb1b76b5007c46e45b3a491640c22a72bf499986e37f55ff50eaf838f4d830fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d198948e0b4a82a089d9f7f8c2929dba2a61fdf42a95c0fd9580ed6fbbad20b`

```dockerfile
```

-	Layers:
	-	`sha256:cf816e885bb1ccccf2e682ad8c98b514cb90e2e22fc2714cc0b11af3b9d3e639`  
		Last Modified: Fri, 03 Apr 2026 23:12:33 GMT  
		Size: 11.4 MB (11350444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72cfcee6c102d7a979328329e6be8f3824d96265c7e6a5fd489d29a1a991eb74`  
		Last Modified: Fri, 03 Apr 2026 23:12:32 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2a44163e8c5f68ced7c321fcbb889752a6231d36dfbf1de44fd8cae806c6a4c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.0 MB (444962014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34c616bedac8e384cb3b44b462eb10243b422e6a745ba5956fa9e5f15da81d26`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:35 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 22:14:35 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:35 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:35 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 23:12:32 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:32 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:33 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:33 GMT
ENV GRADLE_VERSION=8.14.4
# Fri, 03 Apr 2026 23:12:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Fri, 03 Apr 2026 23:12:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:36 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 23:12:36 GMT
USER root
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824d686cb23798401ffbb52de63d20a70fbef48284b9657cc9ff1b95e54649`  
		Last Modified: Fri, 03 Apr 2026 22:15:00 GMT  
		Size: 168.5 MB (168467232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46527ec9af434c7fa6787020904c04a233f849dfcb60169296c957432754fbe`  
		Last Modified: Fri, 03 Apr 2026 23:13:07 GMT  
		Size: 85.6 MB (85602487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aef8f7186d8be59cefa409f4c6b87024af7d6de665d8cbdbd557db54a29e10`  
		Last Modified: Fri, 03 Apr 2026 23:13:04 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbafd5d55cc668a5a0bf5d153e882f2e6d4d192244ab6c6fccca6071dfc670ae`  
		Last Modified: Fri, 03 Apr 2026 23:13:09 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab58834dd82b24825b619ca1af040690f7f9e544c107eae457f9778861cf83`  
		Last Modified: Fri, 03 Apr 2026 23:13:04 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bed024451ce8779f33a8a58c37ba1887ec10290ff8ed1c9cfe03edf82dbbc2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e39f40836ee2af9fe781ca0debf8a689703176f968c88fb56a54fe3168d7df9`

```dockerfile
```

-	Layers:
	-	`sha256:4ad2c7dd0af506e26fce205a307039751f65b933448042ea712223a7cebdc64d`  
		Last Modified: Fri, 03 Apr 2026 23:13:05 GMT  
		Size: 11.3 MB (11349422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2bb4733012a6985f72ebb5b6381d2f2796c0fdcc00eb151c8bf8b70848ba3c8`  
		Last Modified: Fri, 03 Apr 2026 23:13:04 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
