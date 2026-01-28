## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:49c69aa5bf8f0cf5aa97c8fbb02928633241eff527aa444e8e6d2f1f19300b84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d570b09c6cb590ee177ccc964f7cbca7e8f82c3ddb64eec0c14d98de6f9f653f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136382723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04963aeb8e6c9345bed0fea75aa42e87d5e4f020596da357f3d9926e36fcb157`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:43 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:12:43 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:12:43 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:43 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cf50a59fc9eeaa8b42530da305a6f735cf9bc491c46d40089ae331c843560f`  
		Last Modified: Tue, 27 Jan 2026 22:13:01 GMT  
		Size: 82.4 MB (82358887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aa39ae01a981788114e7ea27f6ea2e5cb2a18470fbba15f0d32eee2932adc50a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519f92efb452e3e8d4331d69a08f5d68ab22f02b2cb28fa28b32db6f45255944`

```dockerfile
```

-	Layers:
	-	`sha256:1e032dd478311e75a01ddf37a9e17c5b6294c71a25db767b9810250de0670469`  
		Last Modified: Tue, 27 Jan 2026 22:12:59 GMT  
		Size: 5.2 MB (5182896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eafde451f8d10c9fc25a02bda28f5e80d9e1f4314b03aba71dc35c16b103fe1`  
		Last Modified: Tue, 27 Jan 2026 22:12:59 GMT  
		Size: 8.7 KB (8707 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ca79a7c116aed77d2d87ab41551db6d406f168cd4ad69b51c6967df9c4e7a822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134681556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d758513598590d49063131e5b4868f1eac41665d6025ef3d1d04bed6462ee134`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:11:11 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:11:11 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:11:11 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cc34c74f1a3cd456a80dba19f9d31589c355b8f7bdb3742909b3f364aa671a`  
		Last Modified: Tue, 27 Jan 2026 22:11:30 GMT  
		Size: 81.8 MB (81764918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c592f67861b4ac84ebaf7d7331f989dd6f085f1fb9b6739db7e62aac117b9420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557a5ec8768f963a83e82b5614a251969f60751541d12e88ec01bba1efbc770a`

```dockerfile
```

-	Layers:
	-	`sha256:d404019dd39b9eacf27e02f892297235d9f27596d497e7ceb34f15e68d1c19b0`  
		Last Modified: Tue, 27 Jan 2026 22:11:28 GMT  
		Size: 5.2 MB (5181684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3b21151b45dda5c2135c36bbc9e5e60a069a1940ae3e5c71f6813176a6693f`  
		Last Modified: Tue, 27 Jan 2026 22:11:27 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json
