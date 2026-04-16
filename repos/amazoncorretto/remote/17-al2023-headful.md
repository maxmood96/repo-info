## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c409708cca754d71e5102f66a451e38b03f4831e88f174799a0c94dc956561a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bddb0d618f10bc5e38a0c7685ae32a9be1286e9b50890f5b155e1b17f9bc3f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137651958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bede9e76c2bb6f41adb3998d2ba3df46a53f7a697553ab64f17768bf15679791`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:25:37 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:25:37 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:25:37 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:25:37 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:25:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ccc7790c0865a98386999e5802133490e020447eccd514e6554713d90d901c`  
		Last Modified: Wed, 15 Apr 2026 21:25:56 GMT  
		Size: 83.1 MB (83080704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b46d576d267bf19d3f6eabb15cdd8fadcfe056bbca50812d630db497d305a920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855cee72921f2b2c52ce91438b1092d5cf325bedfb2ac6117ae484c256526f42`

```dockerfile
```

-	Layers:
	-	`sha256:f2a3aedac23314b734e47a44527188010b25580e4c2d54ef8c4a69b7e4ba74d8`  
		Last Modified: Wed, 15 Apr 2026 21:25:54 GMT  
		Size: 5.2 MB (5214769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb3fbb7196569407c80f6f23319eab323722196852251c8130c451258ec26fd0`  
		Last Modified: Wed, 15 Apr 2026 21:25:53 GMT  
		Size: 9.0 KB (9048 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:843ebfc8f28ce9c3a7bd598985eb80479f5496c0d86bf680c0c2d984fc47ee0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135944640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5516847895110a7a96a78cd3021ab74a91ef2c5a409e787df8044c1d26e97b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:06 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:39:06 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:06 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:06 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711131c6f4fa3d60f4680cee7cc91524ed6cd61c93ef584513ff18cd9a491574`  
		Last Modified: Wed, 15 Apr 2026 21:39:25 GMT  
		Size: 82.5 MB (82501901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27229192d92b3eec998883372505bf84409fdb7c7629f7b62751d3189cd2fb62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f5ae86c4348341536eac98e30615898c35e3d3cd4ee9fddfb84e91adff379b`

```dockerfile
```

-	Layers:
	-	`sha256:e68596175ab1ff1bc4182e5dee5d5a9f18f0318fde6d96928ebfbfcc713b8400`  
		Last Modified: Wed, 15 Apr 2026 21:39:22 GMT  
		Size: 5.2 MB (5213560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:540af69fd12ebb76c699288b0075b5b5c57f686f9940a422c2c6e60ac7e5b544`  
		Last Modified: Wed, 15 Apr 2026 21:39:22 GMT  
		Size: 9.1 KB (9128 bytes)  
		MIME: application/vnd.in-toto+json
