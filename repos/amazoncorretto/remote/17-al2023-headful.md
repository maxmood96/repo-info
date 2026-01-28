## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:15381bdc436e5ce9818f926a3811fb3d21f40e10ece7e042ea87384f468ffb2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:21e5de5f6edc6d0aee0a15178f35658c12a53d7525884d3c101ec730e355dbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137106162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248477a048bd2bd516c215177fd918fa222d6734bae938ac470557da4600960d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:24 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:12:24 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:12:24 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:24 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15729f3a4690d76081e486a51ef7b814cb633b1438eea42b11e5e202e9b37f1e`  
		Last Modified: Tue, 27 Jan 2026 22:12:41 GMT  
		Size: 83.1 MB (83082326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3cb674d67884f3187a022fe27caee0b18c762dd4d9a81ca8bff6356f1157d19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ad2c8d9d6ff7ec89c21f56878c25119e0564434d6fec0c45ef9d68d8eb250e`

```dockerfile
```

-	Layers:
	-	`sha256:19dc570275c19b550822b696ceaeb23f18dc7993e99e661c1506c3a98035aa9a`  
		Last Modified: Tue, 27 Jan 2026 22:12:39 GMT  
		Size: 5.2 MB (5208325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6ea49191a8c29f849de2239a951ddf1e6b3e648134a9c4a9b1b7a21da814a2`  
		Last Modified: Tue, 27 Jan 2026 22:12:39 GMT  
		Size: 8.9 KB (8890 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f0450ed692ad2ed2da465fd7fefecefd56025c114f7f95d83e474866b3dfe3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135416647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69195d2c72145475160301d2552ca9c1fde7f27039c242152d91714e9290ed5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:25 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:12:25 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:12:25 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:25 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef29bcc4ceaef7b6b790934f1bd5041d7a24f8bfc0f046db51160a06aee725a`  
		Last Modified: Tue, 27 Jan 2026 22:12:45 GMT  
		Size: 82.5 MB (82500009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:33811f8bd416d6f69203d27e7818e88c9ff5f354a2885e6a7c0277bdf32083ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5164ad7b65ecb407f6a663d4a3ad2f3a3ba063f5ca2e2883503542abd065b8`

```dockerfile
```

-	Layers:
	-	`sha256:eac44b38031669fcf75b756ee4f2c66779142d60c3529bf314e32fd611b77b2d`  
		Last Modified: Tue, 27 Jan 2026 22:12:42 GMT  
		Size: 5.2 MB (5207116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42cb5e0c39b17dfa8020223c414c9abc3059b5b6c34a975188f905ea1af32806`  
		Last Modified: Tue, 27 Jan 2026 22:12:42 GMT  
		Size: 9.0 KB (8971 bytes)  
		MIME: application/vnd.in-toto+json
