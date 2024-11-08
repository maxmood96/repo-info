## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:fe6ffdee0d478ed6df6b1728a8fcc9ae4f591527f978b14b9d547d38b1f8ef64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:99c12d18ba864a4a894eb829e376af770aa5367967535bede200ec772ab578d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135141641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70f3b3723bd21d498ca818bf81d6a36eea6eac5758c3838a8aaddd09625c757`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5f3b500dc43eba4cfdf8e70913f712bd20874deac837800a822eb046b9b8bd01`  
		Last Modified: Wed, 06 Nov 2024 19:16:29 GMT  
		Size: 52.3 MB (52344739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cff32ddd41ba40f5051aba1e5eade2cbd030b02483c598ec88acd80a98b5d5`  
		Last Modified: Thu, 07 Nov 2024 21:48:07 GMT  
		Size: 82.8 MB (82796902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9f2e5f237f648acc9e618f4a7e8be083d77f376c5990a4944f4ec9b03239813e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8adf1003ab7ae4caa2be3275f2ea37d1ea97fbe9e05cf86f3655334e5d28665`

```dockerfile
```

-	Layers:
	-	`sha256:141b474273e123355159e9ddd9fde652453457bee96fac0e6f6c1af68245f66c`  
		Last Modified: Thu, 07 Nov 2024 21:48:05 GMT  
		Size: 5.2 MB (5209861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e4d3f7d9e2b95b01f52473b76c85daa799f0612efea733f8f3a636521ad663`  
		Last Modified: Thu, 07 Nov 2024 21:48:04 GMT  
		Size: 8.9 KB (8935 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fcbbde825d5414568cc73fa41a97dae8969f35d4e9e6fa9d71c33246f8fc13b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133626261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0d57ec4a496817bfb33258d926785158da61f1bfcbf905514c30e04fc0496`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:ec188ec9ab67d19829a9f75d24a165b6b31e1c611a03fdfabfdf4f1950a2c30a`  
		Last Modified: Wed, 06 Nov 2024 22:31:41 GMT  
		Size: 51.4 MB (51424001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7083116b031d3703c5ba9c0833c5f8f14e8a6be10f5213625671862d3c366c52`  
		Last Modified: Thu, 07 Nov 2024 21:59:21 GMT  
		Size: 82.2 MB (82202260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:62ca98fdcd4ab399e3951f79479f9bb3da4176a5e0d96510964c1114f0418a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1603a032d5b8e59ec5bc9e03eadeffae5756c8b82c4ca2817e33db61245f217`

```dockerfile
```

-	Layers:
	-	`sha256:aa85155f3bcba6940182aa8d41b874669da2a668ba55a2b984e32baaddb3693e`  
		Last Modified: Thu, 07 Nov 2024 21:59:20 GMT  
		Size: 5.2 MB (5208650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c022068e6cca6c9ac3d7f5282bde5e73906a4301c13c7fd10b1366fb691575a`  
		Last Modified: Thu, 07 Nov 2024 21:59:19 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.in-toto+json
