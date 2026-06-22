## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:39d13dc7dae82ae8692ea10a219427e4d7fcf4cbf8b1dabea2bd0bef9ec957e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c9dd444ea2f22cb4fcbddb2852b77a38a858af27bbb95a41906fd333da4d7999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144668154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4a8176526923819fec5e5a6b962c152837045268b5e79177e4aa9d5d264ea3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:11 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:05:11 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:11 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615d15657eb013b0e6ca33d5915f473924707a71fe5d049872d7670596afb36b`  
		Last Modified: Mon, 22 Jun 2026 18:05:30 GMT  
		Size: 90.1 MB (90093971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d885f80bf39e9ed1ec6644c6c7572c07229359358ec3618c975cd5c255957fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ee1a975e68c72ff23809150e1bb83456870afd06912b6d5b0119ffa56463ea`

```dockerfile
```

-	Layers:
	-	`sha256:3c2fd75e921d20edc44cd5eb81780763700720cb037222ef0432e7194d1d379c`  
		Last Modified: Mon, 22 Jun 2026 18:05:27 GMT  
		Size: 5.2 MB (5222978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9203c9879bb21cc2c734617e84e51256746cb787fee2600687861a52469b82e5`  
		Last Modified: Mon, 22 Jun 2026 18:05:27 GMT  
		Size: 9.1 KB (9053 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4c8319a0a6ca93584c8f1dd7285daf0c4dc28b746bff15e9528705cafb15c26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142683599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58d6ff319eddebe176697007ee4f2d913cc5bff9063ebcefedeb728838e58d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:27 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:15:27 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:27 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:27 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54d86ce0dd4af5914969b64d9253ba84a47b34459bae52bf065b93c6df1b261`  
		Last Modified: Mon, 22 Jun 2026 18:15:47 GMT  
		Size: 89.2 MB (89232913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f0e0d644fb43420ad805b63da52bc8e725866ab8ef1becea918fca875b0005bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0def7f987404d09258435327058b52ce595929113028d82dcbc8885097c34f5`

```dockerfile
```

-	Layers:
	-	`sha256:60754635401c5af11486e313e44bfdca66f63c665347be9416ca9a361ac62e06`  
		Last Modified: Mon, 22 Jun 2026 18:15:45 GMT  
		Size: 5.2 MB (5221772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb8706d580d38862822f9671af43654e31a0242085a230a4f971a52451051874`  
		Last Modified: Mon, 22 Jun 2026 18:15:44 GMT  
		Size: 9.1 KB (9133 bytes)  
		MIME: application/vnd.in-toto+json
