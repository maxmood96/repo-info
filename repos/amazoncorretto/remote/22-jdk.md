## `amazoncorretto:22-jdk`

```console
$ docker pull amazoncorretto@sha256:8a43bc945068a39eb1629997cf51819d1411562cbdc6eb8d696f2939ac1af5aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6c7e9a262101cd71d45897240eb3ff0d28c53acb6da8a092c330db2b92242e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220924481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c94edd0af1ac95b60db19340f4ef2206238588a84d734f97b26cd24f34ded13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:36abe32954e208232b374495838288731226df866aaad9291ccd46166b252416`  
		Last Modified: Wed, 07 Aug 2024 02:04:15 GMT  
		Size: 52.3 MB (52317903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08fbfe21abc3f0e9505526b28406f7eaafd2e957b62cc35910d4baaec75fda5`  
		Last Modified: Fri, 09 Aug 2024 20:50:01 GMT  
		Size: 168.6 MB (168606578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4265807f0202eee317cadecc30b8abc3412a03b7c9c08b1f61f6e80c3914812a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fd730780b6b2640394896e0741cfe7b57e4aa7bc08a4605fff57010b166a94`

```dockerfile
```

-	Layers:
	-	`sha256:b0c434364d823bf25da9b150732336d4193d4588a732eb7bcb6504fe75d04739`  
		Last Modified: Fri, 09 Aug 2024 20:49:58 GMT  
		Size: 5.3 MB (5319782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06267b44c952f1abf1763a53ca9c78fb1df7da27d195b1983c34d07ca75758b3`  
		Last Modified: Fri, 09 Aug 2024 20:49:57 GMT  
		Size: 10.2 KB (10204 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9e6f6b369d6f03ea080843b9182cdaaebbcbf9e3ff0c65030ec41ace8e511b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218023297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93229fcb1647de5ad08e5df1016e8dca798d0b3f910114dd03107e2c37f06cc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:6dc418e3f016a388470ba66be212f100f862b0633543844e880b17590526cce0`  
		Last Modified: Wed, 07 Aug 2024 03:04:12 GMT  
		Size: 51.4 MB (51409634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf128c9d2f85da2999e8bfcafaa4fafb142ea92b09ada5e84d6f60a6aab9a0a`  
		Last Modified: Fri, 09 Aug 2024 20:58:08 GMT  
		Size: 166.6 MB (166613663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:06098b00d3046fee715098514c1f71a3d2ebcdf53d42b0aaa937a3bf02def33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374cf99a762f2db34dfcbb59d7322d4d4325796f59b6e80ee55e95fcb86b4959`

```dockerfile
```

-	Layers:
	-	`sha256:d4db630d32ad5cc8cd9e478828e50a5ef96c95ffecd7740ced7e376c55e908b4`  
		Last Modified: Fri, 09 Aug 2024 20:58:03 GMT  
		Size: 5.3 MB (5317921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f32410bf5db70f21d5e73825e7547fa10c8fa8e41c7bee8f030c069ceba3c15`  
		Last Modified: Fri, 09 Aug 2024 20:58:02 GMT  
		Size: 10.6 KB (10601 bytes)  
		MIME: application/vnd.in-toto+json
