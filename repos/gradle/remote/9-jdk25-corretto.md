## `gradle:9-jdk25-corretto`

```console
$ docker pull gradle@sha256:cfa3a536ba67402457c0bc75a0e3cd9c4b3148402912ce21a083d17476e09ca6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:c0c698b3852471d1f86690c1663685531a3ad55eb88cd9d7ec301a5cc99f9f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.3 MB (466300459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9371e63ceb50db806ae1fb3151f45fc2f7d6e3f9c71c7d6e3a752e81de631457`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:24 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:24 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:24 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:24 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 10 Feb 2026 19:05:42 GMT
CMD ["gradle"]
# Tue, 10 Feb 2026 19:05:42 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 10 Feb 2026 19:05:42 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 10 Feb 2026 19:05:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 10 Feb 2026 19:05:43 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 10 Feb 2026 19:05:43 GMT
WORKDIR /home/gradle
# Tue, 10 Feb 2026 19:05:43 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 10 Feb 2026 19:05:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 10 Feb 2026 19:05:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 10 Feb 2026 19:05:45 GMT
USER gradle
# Tue, 10 Feb 2026 19:05:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 10 Feb 2026 19:05:46 GMT
USER root
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b81996e3b0e5e4ba9a4cc5fbc9979cd889a255b08bc1d9d4e0dc355bca0f3`  
		Last Modified: Tue, 10 Feb 2026 18:32:49 GMT  
		Size: 189.2 MB (189187292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa7a71b7f4fa78d1f116f5c83aa50dcf1e1511abc340219ebb43d379a7e3eee`  
		Last Modified: Tue, 10 Feb 2026 19:06:15 GMT  
		Size: 86.0 MB (86027942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339802be6ebde335efea7408f191e0a1008687a5229697ae876f3f331b56dd97`  
		Last Modified: Tue, 10 Feb 2026 19:06:11 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0576002eb85c08096ec3636971606f43eb43b2a843697dcae3b18564b7142248`  
		Last Modified: Tue, 10 Feb 2026 19:06:16 GMT  
		Size: 137.0 MB (137019693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8198d3748b7822e6d34d89dddf57484ab998c54ce5402e243a888c0ce182d5`  
		Last Modified: Tue, 10 Feb 2026 19:06:11 GMT  
		Size: 25.6 KB (25623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:35ec088d38fad214fc7253df839fc96e7ea286af6a8af26064fdef2d4acfc767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11360609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c803f286233257eb252c3c20601d956fcc1735f4a20fe411210e36b72947a23`

```dockerfile
```

-	Layers:
	-	`sha256:1c419e2c7ef0167f0b80c9549d04c32fb80d1faab4be5f2b030460ed4098724d`  
		Last Modified: Tue, 10 Feb 2026 19:06:12 GMT  
		Size: 11.3 MB (11338340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a0371332c192101375cb240877abea396a06b9dfe54b3ab192afb436e5f1c7`  
		Last Modified: Tue, 10 Feb 2026 19:06:11 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8122c94c29da3282a12bcd80f84e35b13e22d13114c2214b2da11f5e7d79bb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.6 MB (462572979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d73aba79949a1e4d31b8d096ad44570d87b9c6fd5d9f253d911c573dfb9821a8`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:12 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:12 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:12 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:12 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 10 Feb 2026 19:08:40 GMT
CMD ["gradle"]
# Tue, 10 Feb 2026 19:08:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 10 Feb 2026 19:08:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 10 Feb 2026 19:08:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 10 Feb 2026 19:08:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 10 Feb 2026 19:08:40 GMT
WORKDIR /home/gradle
# Tue, 10 Feb 2026 19:08:40 GMT
ENV GRADLE_VERSION=9.3.1
# Tue, 10 Feb 2026 19:08:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
# Tue, 10 Feb 2026 19:08:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 10 Feb 2026 19:08:43 GMT
USER gradle
# Tue, 10 Feb 2026 19:08:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=b266d5ff6b90eada6dc3b20cb090e3731302e553a27c5d3e4df1f0d76beaff06
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 10 Feb 2026 19:08:44 GMT
USER root
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098ac51664cc3ecb50ec7d80c5020cda656bac5f9d79fc5f5a1093c71586c098`  
		Last Modified: Tue, 10 Feb 2026 18:32:37 GMT  
		Size: 187.1 MB (187088942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531cfa24988f6dc047ef3878c44b131a096c301238c60f97a87c97b6094486d8`  
		Last Modified: Tue, 10 Feb 2026 19:09:15 GMT  
		Size: 85.5 MB (85515103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa9b58b79608e141f1c8132ded4f1e58b0f1f413e0f09a43b6ef958d7d94555`  
		Last Modified: Tue, 10 Feb 2026 19:09:12 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935251e746206c541ae22c04ed2db0c8f3f5c7261bcf1c8be79059d01623eecc`  
		Last Modified: Tue, 10 Feb 2026 19:09:17 GMT  
		Size: 137.0 MB (137019695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f9169f6b494b24f139918dcae92d08c544502d711c51bf98f672cc548b3d94`  
		Last Modified: Tue, 10 Feb 2026 19:09:12 GMT  
		Size: 29.3 KB (29344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4815cf4464484475c3871d282b5cedabccfe3f94cbb7e6f121431bd049f66a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5a1e7960bb923503ef6313f5bbc376341958fd7c541c24df83431cf2c69ff8`

```dockerfile
```

-	Layers:
	-	`sha256:0ef35704444891029281e50945b788cb4b5343912ba01c23b330eec2e4f321ed`  
		Last Modified: Tue, 10 Feb 2026 19:09:13 GMT  
		Size: 11.3 MB (11337377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:641052ac1c6369670f490362a59445561bbb1fa3ebb128f8bc33d5d54e8ba002`  
		Last Modified: Tue, 10 Feb 2026 19:09:12 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
