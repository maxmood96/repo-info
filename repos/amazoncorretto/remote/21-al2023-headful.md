## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:7fe860a7a250045fc73874ad24630a2f2da775d8c3890637a2e80482f5f0b861
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f267bd46fe8ef5c4774a3bea1303360fee56d79f8dd3ef3091fdb814a9e2ed6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143991626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853c8ca74f10e9bb22d3376fe8875197bf2222c0446ca6b228d8eef4dc91b74f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:28 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 23:12:28 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:28 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:28 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40940802b0c16cb118e3f7dc1f7af3088532273c472dc3bae6adf626ad85fa96`  
		Last Modified: Thu, 06 Nov 2025 23:13:02 GMT  
		Size: 90.0 MB (89991123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:207de6c364d7711cea011b4b2cc3b24247a32ff0ff378c08796b8220aa8b02e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bf85160866f3215d19005a21c1411a86de48473a783212b76280d6ff69d1`

```dockerfile
```

-	Layers:
	-	`sha256:d2762379f62d4d272c2637c2f0710c9e084af189664fdb9ae357e7991fc4d366`  
		Last Modified: Fri, 07 Nov 2025 01:50:27 GMT  
		Size: 5.2 MB (5209943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abdcd947040c6270d353c0b4d497e143c2caf9199e88980d41022e5d05445ebd`  
		Last Modified: Fri, 07 Nov 2025 01:50:28 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5032b8c0e99883f69dd53c6ebaf01f5ef5fde5243ac0a3618f36515eb695d6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142032298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1d9e46cd8ea2123b28bd61e121107f81186a1e1e4a163cb7efde669386bb4d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:30 GMT
ARG version=21.0.9.11-1
# Thu, 06 Nov 2025 22:14:30 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:14:30 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:14:30 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f24f32f1fc165df651b9e946515531b41e64a830149195b5ea7c99a421f61f`  
		Last Modified: Thu, 06 Nov 2025 22:14:59 GMT  
		Size: 89.1 MB (89130614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ab506f49438950bf6524e54e331712e1b39cd0be51509ec21b22e3dbfaf66ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee2efbc932ad0119a32c7c02dc3836679dd93f9c28145202ac307ebc39db2f9`

```dockerfile
```

-	Layers:
	-	`sha256:a1c8bbfd5e67c1a2b967aafc00d00ada6bb6f366ecc447c3f017819a327ff6dd`  
		Last Modified: Fri, 07 Nov 2025 01:50:34 GMT  
		Size: 5.2 MB (5208736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6feb4d83dc6b101a682a757fe485cf88aabc5c69aeb649f3998c43d9ae53c2b`  
		Last Modified: Fri, 07 Nov 2025 01:50:34 GMT  
		Size: 9.0 KB (8969 bytes)  
		MIME: application/vnd.in-toto+json
