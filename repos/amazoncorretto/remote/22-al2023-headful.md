## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:40ddd0ed55030e5e32346b76a580e35e61cfca8b155d57476ff6eb3ac47cc96f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9717d74923307e4967a5d0441bb82ce8843418a57295e3277a7a24be85b8c270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141368659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc290e589da191f499e12b19303d25d6aa4d330d781da38f8e81ace2404ab0e8`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60498a819144d3dfe5fffbf1ac087a5d6d723d7404328cd44140aba86649baa3`  
		Last Modified: Thu, 25 Jul 2024 21:02:14 GMT  
		Size: 89.1 MB (89054480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27cd2d197c0c0eae68df1bee39339830a1c7826fc6b25c18b6796428900ca644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fdeaaae7bd323386f7eff05674e1828193ebd85414d15edbbee8c67e789a61`

```dockerfile
```

-	Layers:
	-	`sha256:eb268ec904017d3ac05f8f8b9d068b9b02aefc424aa52bf0294a9b882b8743b3`  
		Last Modified: Thu, 25 Jul 2024 21:02:13 GMT  
		Size: 5.2 MB (5211214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e254fdeee1c585da44150525fecdfe64dc14e841cac75e7fffc63a571c9b99a`  
		Last Modified: Thu, 25 Jul 2024 21:02:13 GMT  
		Size: 9.2 KB (9215 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c710021b82f0183198a258e459d56983392c5b883d8c8abfa0b5ec171af541e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139424202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fdd6adcc216a195e3c3079594f9ccdcdb4b4c68630f0fd5691a241de18aa94`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:69f1520adb0e35dcf91717c80b7867ab26fcf8ef8506b9831fcca72a1b38b618`  
		Last Modified: Tue, 23 Jul 2024 01:08:54 GMT  
		Size: 51.4 MB (51402016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880c87b9307fd97c983eb0f3b321095481969d2a4056d9863d8f666f3c1223bf`  
		Last Modified: Fri, 26 Jul 2024 02:07:34 GMT  
		Size: 88.0 MB (88022186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b6398a61dea46820842686fa9bb5a943f40eef447b408e1f0be0683f393e5b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03d6848cc5d18832916aa22282618704dac94b443693554e16fefd9b8b52d40`

```dockerfile
```

-	Layers:
	-	`sha256:6ca0d1d59c82d99d17ca50db1237f725202e313d1a50d44f13c769f85cff2385`  
		Last Modified: Fri, 26 Jul 2024 02:07:30 GMT  
		Size: 5.2 MB (5209201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ce4b1abfb115780076790b404bba80a73c7a758c1882306cef8291199a9ba02`  
		Last Modified: Fri, 26 Jul 2024 02:07:29 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json
