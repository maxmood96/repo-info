## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:3dbcb6964d9a45a20edd4f9a82732e54d1e960f55710beaf63845604bc07704d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a2bdc2eae33c95496603acff1d3931752d2b6280e6cd0b43f81153357131f96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131278572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4178e896e8b3f3212ab094a0fb4a6fa4c16ed1189400a03b1f4e22e2d2a9467f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:47:46 GMT
ARG version=11.0.30.7-1
# Mon, 13 Apr 2026 22:47:46 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:47:46 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:47:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f5a8b8667b292b4526533daa4ea6a3f8c03cf0cdf4850c99baa7b0e0be312f`  
		Last Modified: Mon, 13 Apr 2026 22:48:02 GMT  
		Size: 76.7 MB (76707318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c68351f8964f727935190b65e49ef355ecf6fd6632a42f2ce4908f3bba03786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d051ff2eaa4f15241d5b9b67750925398827ccc49380fa9cc2e12fc0ddcfcc1f`

```dockerfile
```

-	Layers:
	-	`sha256:ddd484a7ffc4c5fe5178522561ddb977a9701b78ba3b898e76b613ac63068b7e`  
		Last Modified: Mon, 13 Apr 2026 22:48:00 GMT  
		Size: 5.2 MB (5228692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de91498308ac027947a68c378257f27f49d5004852894b8744aa3cb8e8c19d20`  
		Last Modified: Mon, 13 Apr 2026 22:48:00 GMT  
		Size: 8.9 KB (8906 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d68b2a142e383456547792962d8b5ee049efaead1f32e1dfc7e264f6866256cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129398801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3df2b6f2555d2999f56bd5ca99b5657d00f9693bbbedb3f7184a4544b05a76`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:11:19 GMT
ARG version=11.0.30.7-1
# Mon, 13 Apr 2026 23:11:19 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:11:19 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:11:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a179b8ba10b8067f179cb9c12d961a7f6a0e40ccae03618525c04af9d8d964`  
		Last Modified: Mon, 13 Apr 2026 23:11:37 GMT  
		Size: 76.0 MB (75956062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5221050474cfcc1c1654672015049e7e408822109c516fdaf67672f4dade4d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aafcd016b53c71213ce085c2a6ef06231001fe8fc7bf0b66a8202840904d8a5`

```dockerfile
```

-	Layers:
	-	`sha256:5c23e26d2ab803fbf3ca6f561e023bb6c04e4fe289bd82bff7a3bc473d833901`  
		Last Modified: Mon, 13 Apr 2026 23:11:36 GMT  
		Size: 5.2 MB (5228313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623cef57adb18ac93955f0d733637897f8ef410eb851d554785c45a5d29b41f9`  
		Last Modified: Mon, 13 Apr 2026 23:11:35 GMT  
		Size: 9.0 KB (8986 bytes)  
		MIME: application/vnd.in-toto+json
