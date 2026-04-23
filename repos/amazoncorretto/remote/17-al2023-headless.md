## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2b0ce26aae254e16f24c18b328877288d8effe10a173515574977c4182bdcc91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b27dbbf7aeb16f3741def3903857ff993ab55ae0b038b0a03982db5d0a928c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137059774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5225b840763a16a5f2deb9b79848ba39eee24aa01004252e6d793a1d1a4b6a21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:13 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:13 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:34:13 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:34:13 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3ada39c12dc3d8958dd029d874226f8b5aa1ab2d4be953452b2a4f092dafbb`  
		Last Modified: Wed, 22 Apr 2026 21:34:31 GMT  
		Size: 82.5 MB (82488520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5d380efbdde0d64baf25a5b19e6a69595b2bd43012c4db7e6c2194d5419d7aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2961bb54a39d5a55f5063b4e7ef7393188aa3fbb56dbd010d7260f4a85264c2c`

```dockerfile
```

-	Layers:
	-	`sha256:92bd9192108ae298db63132213477ec8c89ef1d8523b5451bee7057b369c6691`  
		Last Modified: Wed, 22 Apr 2026 21:34:29 GMT  
		Size: 5.2 MB (5190163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ddae57061240a6b521ed8242a896a5b7c205bb83b9e12ee5c859b9eb5226b1`  
		Last Modified: Wed, 22 Apr 2026 21:34:28 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:948a006a0cbc85d291df3a7c91a973a26edf4506eba709819c17bdd17316bd76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135342811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b01cc87e49860dd5084ef3d145db893021e090eae4de3b839464cb95780d094`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:15 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:15 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:34:15 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:34:15 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3e6065d70c054d84707b40aaec6b472370dce49684c8aa79fd40b6a84ced13`  
		Last Modified: Wed, 22 Apr 2026 21:34:34 GMT  
		Size: 81.9 MB (81900072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b362b78683ef28f6289dfba6586f89c2383d11fe3c9c9fedd6c246cd919e82d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5197914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40ccc8eaa929a8eb451374be482d9740180e8fac7424d5a5732f2edf35aeb74`

```dockerfile
```

-	Layers:
	-	`sha256:4cb4f3bf3ef0ee5c3ad8ed3a0f116bbd5347e541e9e1178f12696679bbf8118b`  
		Last Modified: Wed, 22 Apr 2026 21:34:32 GMT  
		Size: 5.2 MB (5188952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa9d7f8e7c47ec50840abbc2b9275b3c1998093f32ee3137d9343a4269d7882`  
		Last Modified: Wed, 22 Apr 2026 21:34:31 GMT  
		Size: 9.0 KB (8962 bytes)  
		MIME: application/vnd.in-toto+json
