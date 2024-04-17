## `amazoncorretto:22-headless`

```console
$ docker pull amazoncorretto@sha256:208fca462f9859cc0eca209f308a4297de8c10140e57f7cb24ab68395373756b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fbf581e70699f833d724803494084c83bd20b9051e87b1d9871d68fe2a200a22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140926786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b636bc8592d3c797c945d093aa8be3b8b2767b842f9a5e19b33381b6c074fae4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:21:43 GMT
COPY dir:78fa4f6b1d2d2862367cf50eabd290fdf95c6fac76e06e7e2e34c2d4247bf889 in / 
# Fri, 05 Apr 2024 18:21:43 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:06:41 GMT
ARG version=22.0.1.8-1
# Wed, 17 Apr 2024 00:06:42 GMT
ARG package_version=1
# Wed, 17 Apr 2024 00:07:27 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Apr 2024 00:07:28 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:07:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:81e74100301dffd9fca7e4378ed7aecb21d613798689a5481ed8365657bf5efc`  
		Last Modified: Wed, 03 Apr 2024 01:55:13 GMT  
		Size: 52.3 MB (52323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abf38b82bb0f272e2e8c10f2628531939515ef2d2a6889379b3c9da3f202dfc`  
		Last Modified: Wed, 17 Apr 2024 00:27:35 GMT  
		Size: 88.6 MB (88602881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5415603300739f11e5962e5f3233ffd957a90a940b26d6a89ed12a8a2a66a42b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138972949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678acab1883e030a3619716452d8ab928deaebc216562dc8b1963d1c9f67ac41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:15 GMT
COPY dir:f8d39fbbd7bf18543727aab8c7ebde8152233a1cedabf00f365356d7779f0166 in / 
# Fri, 05 Apr 2024 18:07:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:15:39 GMT
ARG version=22.0.1.8-1
# Wed, 17 Apr 2024 00:15:39 GMT
ARG package_version=1
# Wed, 17 Apr 2024 00:16:16 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Apr 2024 00:16:18 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:16:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:2db99c85d8118887d64b46dad6e559ea58c1ef5620f9a766cd0658af1ec030d3`  
		Last Modified: Wed, 03 Apr 2024 02:28:44 GMT  
		Size: 51.4 MB (51408325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e817c2761881f9bf333077db1d8322c8d20aff436e313f660179b685b40a216`  
		Last Modified: Wed, 17 Apr 2024 00:36:30 GMT  
		Size: 87.6 MB (87564624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
