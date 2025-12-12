## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:37b83e90608bd0cd8db51e5a075af05b92a3a2740e6c26c24bd34b7e267361d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ba9d4c67141377139761c7d5b31e30a68ffae945b2694e380f78cb04445268e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158290265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61d25f186b1ec2786427b66884cbe69cdc6f0c367c76c4b10dfa7cbe5222391`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:31 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:31 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:31 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:31 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396e0a4e16d7e07d7345f40bbb99261a8675b06d96a649a831b9493dfc2493df`  
		Last Modified: Thu, 11 Dec 2025 22:14:06 GMT  
		Size: 104.3 MB (104301805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:93170cfd2e37bd92dc8392106ae026fee14a5ab26d09ff594300717e5edad420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:841468e8ec8ec17b20990e7a4ba83c5d0b31ed66f47adfd8a5e4d5b8455fdb8d`

```dockerfile
```

-	Layers:
	-	`sha256:220d5eea39f88e96687f95d01b2408c46173524b17bbeb866c5e6c0d4c948475`  
		Last Modified: Thu, 11 Dec 2025 22:50:49 GMT  
		Size: 5.2 MB (5220208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3956605671677b344c1d2c45fcb2dfe90dc78fb3322b12d03c8718a32aab9a2b`  
		Last Modified: Thu, 11 Dec 2025 22:50:50 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d1552147f311853ee295c10e496475da55496b03a9f57dd6d546370c9c1f6b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156116399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d7b3802040dbd817b1f480adb72fbdb104f00a6a5d8cc9c8f4a8c5e860e5d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:02 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:02 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:02 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:02 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87a8926a455e83f53c4c4da43308395246fe09966a7c954bf902aed9e34cb3`  
		Last Modified: Thu, 11 Dec 2025 22:13:43 GMT  
		Size: 103.2 MB (103242949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ca96920e83045ebccd1ad59378a6cd8672d6a5b691f0e6004566b1427378eac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2263c4fb8e11253be87f44b8c3aab0ee0f47594199f022df0913a7e685aba442`

```dockerfile
```

-	Layers:
	-	`sha256:72675d7ad086208f8c446e688a29d692ca4ab4b21240ef2033154cc6d83a366d`  
		Last Modified: Thu, 11 Dec 2025 22:50:55 GMT  
		Size: 5.2 MB (5219022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d30546d844ad2e300ac3fe8d3c6dec5edc40d411f6466694029340edfd7ab90`  
		Last Modified: Thu, 11 Dec 2025 22:50:56 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.in-toto+json
