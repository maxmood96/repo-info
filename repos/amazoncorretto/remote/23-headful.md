## `amazoncorretto:23-headful`

```console
$ docker pull amazoncorretto@sha256:3f9ce66615b6fa1e11620dce28cbc1630d6fcd58245097c32e0afc703865b245
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0e597090a19cf35a891da006bfc0f7d3bf802fdb15eb2e6a9fa82ee0a4fcef56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149866613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1a426c253addc94a0e412d9ab273b580ec62b48c576975abc6ca4c666d1aae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=23.0.2.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff496c344df085754666a6a320560349df1cd4bde56baeac577a251c51d6ed59`  
		Last Modified: Wed, 02 Apr 2025 00:02:04 GMT  
		Size: 94.0 MB (93959560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1cde0d14809ec508f5c0eb0857e449d6051293220abe5831037d5c8135bc69fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5578357fbe15c4f48ca908f2eb8abe6eaf731c094e4aa40af6f35f5c3af55bb6`

```dockerfile
```

-	Layers:
	-	`sha256:472e633e6c2fdab9dd242ea6a9a8ec73297df170b149aab1d8c8633fb99bd194`  
		Last Modified: Wed, 02 Apr 2025 00:02:03 GMT  
		Size: 5.5 MB (5455466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f828d805107bc9ce56a993a54a46f1b74883b7405e79bc7610972960f03ee9fa`  
		Last Modified: Wed, 02 Apr 2025 00:02:02 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b11bf740e4062da27cadc04663bcd691e481d74bde20617c37d59db3109751b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147931937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f8d06b4179d539c437bc74bd636bb17dd14aa4d45b2c577b8088480881907b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=23.0.2.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54d4fac9daaa80b14510dabd9ed99108b1353422f25bd69727ba4706d1765da`  
		Last Modified: Wed, 02 Apr 2025 00:37:20 GMT  
		Size: 93.0 MB (92970928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f70449f037d512ea8fecb17fbd78b7ae43b130d8d25ee0c47458d9bbeeeae08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5462798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984a4098313f406a7f045dae115f463f3e85cce176775085af96eeee9a192c85`

```dockerfile
```

-	Layers:
	-	`sha256:10dd24f8eaa62a8b6b6bd1c984b0a59892913f55e8f94677b1d6745e32df0d40`  
		Last Modified: Wed, 02 Apr 2025 00:37:18 GMT  
		Size: 5.5 MB (5453458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d4f82f8fcdf99500e5ff601c7767042deedbe1cfca9026755dcbe6a367be37`  
		Last Modified: Wed, 02 Apr 2025 00:37:17 GMT  
		Size: 9.3 KB (9340 bytes)  
		MIME: application/vnd.in-toto+json
