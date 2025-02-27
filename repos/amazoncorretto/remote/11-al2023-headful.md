## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:9a4817341992fa35d0b06ba86b0dce8d86aa525103d19dee7a7deed4c5377904
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5e7560ffbcd4a5666d5f696fc759328cb05fa8ad179b0f770739be15ac5a2d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130093690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51a897ecb1e85a151084452df6c11c7d20d0157802d640dc7172aec6d2dd60c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076d060a886b97184fd924c968724fa51ef7397ababf93304999589d8cddeb64`  
		Last Modified: Thu, 27 Feb 2025 21:08:10 GMT  
		Size: 76.9 MB (76941957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5316034a1456a92a5ffdbc11789de38a4158010acd237aefbb146bc51a0d8270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67bba8297d5b7be489d6cdf95d3ac3c017dc92042fdd5f17414ae8e7bae33cc`

```dockerfile
```

-	Layers:
	-	`sha256:15a0bee3fbdff559c2b5596525c7bf6b180be09578bb7ccaa48fab8b1378cbc4`  
		Last Modified: Thu, 27 Feb 2025 21:08:10 GMT  
		Size: 5.2 MB (5198885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edf6f50f0cb241ec2824a556e2e1b45dd979a4287f768bda17368b95d26e530`  
		Last Modified: Thu, 27 Feb 2025 21:08:09 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8703668dda4885b82d0d0643f197328c734309a5828edb4b5c83b1899767a3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128397796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096e0f9368da829b17a11e6d2e32fe516cd3f190c7b83132482ec5c543dbd743`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0d30291008c8bb5afb5684e91c5e49eefd24a3559b729ab1aa73eab4bde305`  
		Last Modified: Mon, 10 Feb 2025 20:17:28 GMT  
		Size: 76.1 MB (76126845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2cf672142599ce3d1f3e45b0abd6c3691e1a309b003fd51d5534621b590c78a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961bddc9517b9175fd2af00ea95485aa6be663dc3806fb73e8551559b09541b`

```dockerfile
```

-	Layers:
	-	`sha256:23a26156595f3afce2c03d5eca92d67ef8b5328e0f15530c982e11216ac5abd0`  
		Last Modified: Mon, 10 Feb 2025 20:17:25 GMT  
		Size: 5.2 MB (5198506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec81e035fd22d1e72100ed00cbacade711939097f7177ce124e1c86af5a2da80`  
		Last Modified: Mon, 10 Feb 2025 20:17:25 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json
