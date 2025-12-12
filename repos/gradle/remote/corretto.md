## `gradle:corretto`

```console
$ docker pull gradle@sha256:f6a2d76f1b3f8a528b88441aa0e196e4099e121b744cbe90476fc9601ce3bb58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto` - linux; amd64

```console
$ docker pull gradle@sha256:0fef42243943d544aa93e37c3934e59b0125907a8bb4cc392dbc631890224c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.7 MB (464722397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101e8443259a4be7b01d1a374cb5f2bd1318fdcdbd43d53745057514535b1a79`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:21 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:21 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:21 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 11 Dec 2025 22:17:50 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:17:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:17:50 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:17:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 11 Dec 2025 22:17:51 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:17:51 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:17:51 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 11 Dec 2025 22:17:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 11 Dec 2025 22:17:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:17:53 GMT
USER gradle
# Thu, 11 Dec 2025 22:17:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 11 Dec 2025 22:17:53 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91413819017580b0cad6a6036474dd8d9101d5528fc612f3e8b639ab91f6de1b`  
		Last Modified: Thu, 11 Dec 2025 22:17:29 GMT  
		Size: 189.1 MB (189138728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf0ae2a06d69f57a69a48a61d3b89ad4e14b54bd0028f327e55e0283235f67d`  
		Last Modified: Thu, 11 Dec 2025 22:18:40 GMT  
		Size: 86.0 MB (86016663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954e2726dbd1ac161c1cda8116cc7784f17017030d87a671b724250562c1b028`  
		Last Modified: Thu, 11 Dec 2025 22:18:29 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d0bdc455206e4ec636eecb699153e15d6b1f9c7e51a3066959176ee7b744b8`  
		Last Modified: Thu, 11 Dec 2025 22:18:55 GMT  
		Size: 135.5 MB (135521965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c0a2fedbfe953aa25a1e439d63bfc0b3344b631daa9d38e0e8a8c5be28a31c`  
		Last Modified: Thu, 11 Dec 2025 22:18:29 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:30bcac11944a542df0d8543b73839cc8a058bbc1469187f2eec8bc10101a1324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af03b8202ada4ee0ac19c070706912c0b19772c7a312a857501b30389cc2dfa0`

```dockerfile
```

-	Layers:
	-	`sha256:0e7b84c240e8e6cf6d4ad7b31d80583597a16a8df066cb64d8c01502ecdcdb4d`  
		Last Modified: Fri, 12 Dec 2025 00:24:00 GMT  
		Size: 11.3 MB (11349337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b227110a396331bf9351e80c8bf638428084c0d50d2042c70d17c62b33d68c`  
		Last Modified: Fri, 12 Dec 2025 00:24:01 GMT  
		Size: 22.3 KB (22268 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:0739d0c6693caaee609415f38c3e313bb612f3c01245b17b783b3a95a13792ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.0 MB (461039601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b274c4b7e39ce08d1e60225c960ab8d7edeb20ce7a610bf1e62e4b27fcf2ed4`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:00 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:00 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:00 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:00 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 11 Dec 2025 22:17:35 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:17:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:17:35 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:17:35 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 11 Dec 2025 22:17:35 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:17:35 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:17:35 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 11 Dec 2025 22:17:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 11 Dec 2025 22:17:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:17:43 GMT
USER gradle
# Thu, 11 Dec 2025 22:17:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 11 Dec 2025 22:17:43 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddfd06178dcdca2a5cd3684d7be72c33b03527be5f3cd9c8aa6e0db1f16ac0b`  
		Last Modified: Thu, 11 Dec 2025 22:35:49 GMT  
		Size: 187.1 MB (187059439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcd90ad71288e195694ff154eb03782fcec6288cef4eee92315d541521e1810`  
		Last Modified: Thu, 11 Dec 2025 22:18:31 GMT  
		Size: 85.5 MB (85523542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269ed1184924d1d7951b529b682167ce70e6d8a251e59896a1a9a112fb9b87e5`  
		Last Modified: Thu, 11 Dec 2025 22:18:22 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cd75dc902a0f7766b99bb8abaeabb053a13e16c7effd88cb9fec542267baf9`  
		Last Modified: Fri, 12 Dec 2025 01:19:54 GMT  
		Size: 135.5 MB (135521968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61596bea73f86db63e6b2f43e5c8f84769d36ce80e7be36df2912b401f5ac41b`  
		Last Modified: Thu, 11 Dec 2025 22:18:22 GMT  
		Size: 59.5 KB (59524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:1d524db8ba9de16fd1fcc993ff5ed3b8fb3be48ffcc4a246d776ce48b136bade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dc2ae5f3764b6e88583ceb6ef3e04b0d9d4ead2f83affa680dbc14d14f646c`

```dockerfile
```

-	Layers:
	-	`sha256:e2280c578063a75b107be8ebab3954f54398a2ea881d01285264e1255adf9f21`  
		Last Modified: Fri, 12 Dec 2025 00:24:10 GMT  
		Size: 11.3 MB (11348374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49585244d27c8508062e712fd45f2e7500cb624cd1ae1a46730e18fda00c6ba5`  
		Last Modified: Fri, 12 Dec 2025 00:24:11 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
