## `amazoncorretto:26-headful`

```console
$ docker pull amazoncorretto@sha256:2d3b136cc46f691fed2d64daeab8b273b83c0bf3bc9e5fa44a264096d709a834
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:57bd3ab0de7115b60db2b7e6d9abbb516bd945538c7696a72b8538756a72a242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161111711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbeb9a5011618fa4c03aacb2ff3caf427971f1cf409f36e8e060a15769075c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:55 GMT
ARG version=26.0.0.35-2
# Wed, 15 Apr 2026 21:26:55 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:55 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:55 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3c89acc7a6a3cbfd40ac3258700129e763586cc51451e72d6211ba7426a176`  
		Last Modified: Wed, 15 Apr 2026 21:27:15 GMT  
		Size: 106.5 MB (106540457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4d68d9c17f33ed692992bde52f1b3d6373a70d732b0c363cf689fac93cf65c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c73930548ca5b8467e628549583345e49b9f318ed2dc0c27d74f49ba5eca8d`

```dockerfile
```

-	Layers:
	-	`sha256:f80f326a3229b298c3964e52dbc013acff028ffef4b9c9cae33474354ade83a5`  
		Last Modified: Wed, 15 Apr 2026 21:27:12 GMT  
		Size: 5.2 MB (5225831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33d961a4a90f143d27dd3c87a62b5e58c635e83651f9befa6d7168ff01449612`  
		Last Modified: Wed, 15 Apr 2026 21:27:12 GMT  
		Size: 9.4 KB (9369 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ecc677527c02633adb7cefc246242a83f12f939bf8127d4f14e485a6ce25f615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158876975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27d16c55ecb6b934997e8eae0150c82db964f876cc417b1380c595581ed328a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:40:04 GMT
ARG version=26.0.0.35-2
# Wed, 15 Apr 2026 21:40:04 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:40:04 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:40:04 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:40:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd1de0f89706161275ba9d32023043697b3fdcaf6c360516b7e0d669772159`  
		Last Modified: Wed, 15 Apr 2026 21:40:25 GMT  
		Size: 105.4 MB (105434236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e0b326c4be61a0c163d138d9846cfc6cf8d51d0aeec8a62c89cf8abb57c4d5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1394c3e59cdbec6ddc9402033b43f17add55aa1aa19f406cc45953d7fb97e6`

```dockerfile
```

-	Layers:
	-	`sha256:b26dabd64f55e6b330cc04ee78c867af5b8b570efa602efbc4411775973ffe33`  
		Last Modified: Wed, 15 Apr 2026 21:40:22 GMT  
		Size: 5.2 MB (5224644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044fabd37373b3eddb7d3802295dde67046afd33eec100a177768798ef39fb07`  
		Last Modified: Wed, 15 Apr 2026 21:40:22 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
