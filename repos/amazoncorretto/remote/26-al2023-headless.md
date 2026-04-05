## `amazoncorretto:26-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a4b9b2aaaeae2bebd4c323c80515ad9ad5c864c3f4b447eb17bc86707a982a99
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fd8bcd2be65d48a66b053e2b4dea3e23f844ba8e8c167693f40233edbf2e8250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160396825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d82c939ef2543a649a23650ed64df3552852e0596c86355c31f157718506988`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:15:27 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 22:15:27 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:15:27 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:15:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45ab9dc4a4e6532a7d3063893a4d496e4d12b710b5b36b2c5452391ec7db570`  
		Last Modified: Fri, 03 Apr 2026 22:15:49 GMT  
		Size: 105.8 MB (105825522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a3e99e2e3726fce441019f66e7c520decadf9d6bb789411cf01201d3ebc9951e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29673dfb90655f5915c8d6da1109e7722799327395b2a0af8ff50fc187be0bfe`

```dockerfile
```

-	Layers:
	-	`sha256:974a763092db1fcbc5a35123b82cfebd2630b6de18a83f195f08ec6b3a2d237f`  
		Last Modified: Fri, 03 Apr 2026 22:15:46 GMT  
		Size: 5.2 MB (5200404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab56a3b84adae5742fad0e0f9463b25ed4b2a7105cdde6260dbb4fda941271d`  
		Last Modified: Fri, 03 Apr 2026 22:15:46 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7c9f1008b484d7b98d45ad2eaac3f29de7f92c611a2e79941293e264e0d07553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158150812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1d80082bc6fe95f936f1c62d981489436c17b4cbc03396413b8e5059b7c73d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:43 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 22:14:43 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:43 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:43 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043d817b7046761ea0d81fe74e34f55adc461c082bacbf613ed729256c2d0f43`  
		Last Modified: Fri, 03 Apr 2026 22:15:05 GMT  
		Size: 104.7 MB (104707987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:206b30676b927dc66ee1706eaa672f516deeb2fb869caac3d0e6d2f3af14c85e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8386ca42caa7276f2a2e9af6619dff4a22ab36ec3914ea2972cab6797ab229`

```dockerfile
```

-	Layers:
	-	`sha256:e119f12fe8e45e4f49723af2435e98eb1469ae1bc47186aef745ef954bda4fcd`  
		Last Modified: Fri, 03 Apr 2026 22:15:03 GMT  
		Size: 5.2 MB (5199214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a47418c36b3216ea1e234c5ddf24d86ef2d807890ae444d87c7000e6ae79df4`  
		Last Modified: Fri, 03 Apr 2026 22:15:02 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
