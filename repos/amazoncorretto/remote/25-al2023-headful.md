## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:291ec53ddb93391dcfd99597221510589c8410f8f56df5ea26857aa968b4e414
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:20237a12f6afd4a6167b1348e6705805975584f5d572cd35520a18662dfb388b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158323920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c867a7b00fee8fed86783b6ed1b60316215cb014960488df2099e3d6f497120`
-	Default Command: `["\/bin\/bash"]`

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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1baa50416fee04a0a697c4f651637117a914f11cbbdc557f1311714490c7ddb`  
		Last Modified: Thu, 25 Sep 2025 02:17:29 GMT  
		Size: 104.3 MB (104318640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8573402b57ce1305e36b680d7a5ce082e13e9597e0ffad3e03ddba178a84fb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d254e72f8545f4aff74e98686f3fe782358ae0e3ff9d5a75079b60d74180433`

```dockerfile
```

-	Layers:
	-	`sha256:d672aaa79691b423309ad3fa8e79d576aae086b7dcd19fd0e9456efb14ca9601`  
		Last Modified: Thu, 25 Sep 2025 03:51:55 GMT  
		Size: 5.2 MB (5220130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:011a54e294ff6c48fb716664c3c8e3df45912a312a717ee1d0b49a3a32022009`  
		Last Modified: Thu, 25 Sep 2025 03:51:56 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3e91128799f68ad392cfa165f64fd22d5ff415ccf39e60491e5eff97cfe61ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156135733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5883833b7d55bb9cf82a37c331606b4d2be59f953db2007292c84a05e87c563`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e759c49ff3c25040555c9afec2c05ecb98a3c8bb24b6f52f513cc343e165cc`  
		Last Modified: Wed, 24 Sep 2025 21:14:35 GMT  
		Size: 103.2 MB (103236295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e5971cc6a785fcecc7680426a9b271034db9f8bcc48d70afb0536be376773476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d7e459d25be7e3acda7f32bd7981ccfeb5bf6e9a8c3b20a9b18962a043b8ea`

```dockerfile
```

-	Layers:
	-	`sha256:d1ba7fcfb05a76f98f84490aeff4be3530bc61d871b249eea092356dcd0577bf`  
		Last Modified: Thu, 25 Sep 2025 03:52:04 GMT  
		Size: 5.2 MB (5218944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba4aa24e79900c05cc1e74c5f21a3f70110899ec6e64e33e5f5b1e10d17cfa86`  
		Last Modified: Thu, 25 Sep 2025 03:52:04 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.in-toto+json
