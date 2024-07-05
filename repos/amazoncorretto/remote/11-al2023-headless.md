## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:f5e014d01a6e8df40315076ff4424274e4d0d83d45a279b0c4e744887a3070c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b3e68d41a9b130ab4794a59407f3417d754d757eb0d00a096b1d07ff2a1ffa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128471554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdffa01df2b67e9fc8c1217d337ebcc9bdba5789e29b5b088568ccf716b697f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:1c9e0f4db95e1ae683b8f16b1ecfc5d8693ad4e5e379a2386e2870f38383c7d8 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:860904071dc658e37de73aa1556e7badfb13bef4747965ea3bd1049e8ff87dcd`  
		Last Modified: Thu, 04 Jul 2024 00:20:13 GMT  
		Size: 52.3 MB (52319623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a35ae18100d5ff0e42d20bbcf838887050fd2801596f508f0e49251a0a6f82`  
		Last Modified: Fri, 05 Jul 2024 19:56:34 GMT  
		Size: 76.2 MB (76151931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8ba0ebe46fa17633cffd3efdffa6e41cec72ce992de53b121d3adda477cacc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5180059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52070b3f468805094a82701679700a8abb6bbae9decb851486edeed941e8ca6f`

```dockerfile
```

-	Layers:
	-	`sha256:1541b3024a221e30107267ae4cf2ab698d6942e9eae803540dae6c3b8ccac677`  
		Last Modified: Fri, 05 Jul 2024 19:56:32 GMT  
		Size: 5.2 MB (5171637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb9ae5de5da83df5730a57068f3d27bd2fafacdbfd1de1bce285060c19c2c03`  
		Last Modified: Fri, 05 Jul 2024 19:56:32 GMT  
		Size: 8.4 KB (8422 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f682a1e234b840989488ad69cd24399fbd7639d72a9e07ae36524367a472faf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126712767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db82931bb89eeb3f2ed0bc85a1af12d5472d6ee143b1a4238be8aea5c931a418`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:a2f5453af1f2210c7b49fadc5acdaaa335139ac35c64847d2f5879056f91a03d in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f95af119e05065dbdff89fbd219657362e32f7ec50d632e28754e75b5a13806e`  
		Last Modified: Thu, 04 Jul 2024 00:39:44 GMT  
		Size: 51.4 MB (51407040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367dc95a8016dc0ae15ead2d668836e2ad76d229bfe085f474562958052469ba`  
		Last Modified: Fri, 05 Jul 2024 20:05:11 GMT  
		Size: 75.3 MB (75305727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d24492dcf1d8a47c15e9f336f40848d41820cd9f0d415a67eb828b9e80d2aeae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5179956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73f0c3d858a0fd6336a933375a4f102fb4d1fb4caa22990dc8a765779855532`

```dockerfile
```

-	Layers:
	-	`sha256:9265d53a32f92b7aaf3639e1b2fcb674a8ee061ba80f4aabf0eb4f6edcd25372`  
		Last Modified: Fri, 05 Jul 2024 20:05:08 GMT  
		Size: 5.2 MB (5171253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b607d183b20c11929e871d88632a9d2945e29a60957759016be5a849568e3598`  
		Last Modified: Fri, 05 Jul 2024 20:05:08 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json
