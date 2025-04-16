## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:4a954ec45437af68db620c80ac20a317db9ae98f7732e48f8efc2c7122ff90b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4ecfc13a157e68620998b408b5ff595441b169d6fb136866263214f8e654c8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145724652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a351f0f1a62f22136063c2b4d19103240483b15d1d126580b806dc82b9f7f1fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:23 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:23 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e0178fe4eb881714997666f3f595c8c65af600c15292feaaec506a16066240`  
		Last Modified: Tue, 15 Apr 2025 23:56:22 GMT  
		Size: 89.8 MB (89817599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:90d0e1dfca081024535c3279459286149ce6207ec848f2b68d668e6c72ee69d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ecd5fa9c90734e1e472f9248d16d1c87ddb3114ce64a26026595ab561bdb7da`

```dockerfile
```

-	Layers:
	-	`sha256:fcc64773f0854e80229cc55b68d0235d3a8a357595c3dbccf895cbce33128ab5`  
		Last Modified: Tue, 15 Apr 2025 23:56:20 GMT  
		Size: 5.5 MB (5452644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74ffcc159565fa90278a07737880fc5d500c2b04f3ed49e106af5a262c78544`  
		Last Modified: Tue, 15 Apr 2025 23:56:20 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8f0b243ef80b6df41d5639c3ee6f8044d21f51308592a5609b5af99d9fbaa548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143897405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3552f14f3358987c690cd3204212e424f53a8be356cf25d3008e02b8b70b97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4675159c23acdb63333fb3bbb9eac6cb0a9233e4a51d087b279aea20244d979`  
		Last Modified: Wed, 02 Apr 2025 00:34:41 GMT  
		Size: 88.9 MB (88936396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de3f4b71d8a24e7c3666a544efa73949b95088ec989c4762ce7046fcc2311473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116d7779ee258f510b881d0ab5a8e0384a58fe02853a501cf8c4aeef506dbda7`

```dockerfile
```

-	Layers:
	-	`sha256:618e00ab4f5ce3e379da72176893955753381d204b0835b5496e7000d630bc9e`  
		Last Modified: Wed, 02 Apr 2025 00:34:39 GMT  
		Size: 5.5 MB (5451437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044c49a453d8ba89d70d3700c8fa6979fb63f016d99d9a2ec85943abc95a2c47`  
		Last Modified: Wed, 02 Apr 2025 00:34:38 GMT  
		Size: 9.0 KB (9007 bytes)  
		MIME: application/vnd.in-toto+json
