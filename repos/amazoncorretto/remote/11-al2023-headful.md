## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:910250b857da47f0550308262a10022b76d546d03a2b6379a5d589c098c01f9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ce030d8f1df11906fcd1e314e2167aefbcbee4a5750bcb58116f49f8036a6feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131337404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012dd796bf93de7ed57f206fc25060f5c3357bb4d6b81e85a40470fc8fe089f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:01 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:05:01 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:01 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f0d1d7708d06d9e320c005ea4a287bbd70b37a47af1347fb2a273c1ee414e8`  
		Last Modified: Mon, 22 Jun 2026 18:05:19 GMT  
		Size: 76.8 MB (76763221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:70383d23a8abcba315b379852ce3078f2e2c09e19551c7086b7bc7b9f845e747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526db6c27ff5fe17108a49afc230401d2ed5f92bc921cb1f95c16a6cf19de62b`

```dockerfile
```

-	Layers:
	-	`sha256:c964c799ca944d165eceb76450c61d3fc48e14adefc7d3b260998a814cbd0f32`  
		Last Modified: Mon, 22 Jun 2026 18:05:17 GMT  
		Size: 5.2 MB (5234456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1b9b97e49d28a0a940d57b0b3f7c9f331b378a54eb52ffab4a2f761e385ea15`  
		Last Modified: Mon, 22 Jun 2026 18:05:17 GMT  
		Size: 8.9 KB (8907 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:74843c7be74ecfd6497e4d958e84169d86da7969f84580cce0d22788529670ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129466206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b94352af6312be3f5063aa653df7cc0bc39f5fc95d552876db7187772899b61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:14 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:14:14 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:14:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f401903dd2b9245f0bed5170c58fadca812dc4a3f00ad9f534dca7f64eb92e58`  
		Last Modified: Mon, 22 Jun 2026 18:14:32 GMT  
		Size: 76.0 MB (76015520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eb4cdde2ecd505fb17df7020d11d933deeadf741552ba62cf18715ea28369294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6647fa502268f5f220ca284c311065990be3093b2296ff3024cad568d5df804a`

```dockerfile
```

-	Layers:
	-	`sha256:05ca39e2d4c86dcc5ae49e14b9e172bb1a2941c870a7b7de596868b9abf5f56a`  
		Last Modified: Mon, 22 Jun 2026 18:14:30 GMT  
		Size: 5.2 MB (5234077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5753e39fd00090e83f112ecbfa2d727a2dccbf943fa9464d9a33f09aecb74f75`  
		Last Modified: Mon, 22 Jun 2026 18:14:30 GMT  
		Size: 9.0 KB (8987 bytes)  
		MIME: application/vnd.in-toto+json
