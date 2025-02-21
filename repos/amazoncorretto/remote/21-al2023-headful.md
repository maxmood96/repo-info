## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:5c123167b73fa32c54f676b9fa7404252414853148155ed39bcac7262bb21d25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:392e57a684972745ca2a03f819b3410aeace95fa9e6caf36a42270b27afdfde1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142836666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32d3a40029484b8b9526dea9372688cc713d7e3eac34a99ba2ba455de35fb0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aca28cbb53e9057270c51fd4f48300327ad901e786ced10b7d65bae8df98b5`  
		Last Modified: Mon, 10 Feb 2025 20:08:42 GMT  
		Size: 89.7 MB (89686083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7f00974aef828cb7497bd9342d5146cf215a559d1ef7d38d26d0a3c85792046a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5195504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3b24c87bf76263ac5a0c3ed57bc7ad0e698d66d5fc337a47354d0291577eb5`

```dockerfile
```

-	Layers:
	-	`sha256:cc66338de2fdeb8c66e021cf27fd2b3f5c9c94023e86f988d3c61ceabae65b66`  
		Last Modified: Mon, 10 Feb 2025 20:08:41 GMT  
		Size: 5.2 MB (5186578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd84c6bd229295261cb0ae6a4ad29fea79044828c9db7abb9a5147e4ebab575a`  
		Last Modified: Mon, 10 Feb 2025 20:08:41 GMT  
		Size: 8.9 KB (8926 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:579857a98d65c60df3bfd4a9a80e0976f2e9e25d636391ca6db64542c6f2f531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141104443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f39e5c3530c657b190b27585685e2830d4a435b4f2984e5a4e3b2c1344f300f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290435f62bcb3d86ee633eae382fdd66254985a60391f6000db3035bd39a71d3`  
		Last Modified: Mon, 10 Feb 2025 20:28:45 GMT  
		Size: 88.8 MB (88833492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:60892d06e897e2346d998c0085b6c0f216619ee86ebe9461e39d451ac7cf1645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997e73607861a908d56314e6fb756edff4ec54fc8afdfc796de7333de4db1760`

```dockerfile
```

-	Layers:
	-	`sha256:176fa5293f124d9588ffe5ec5c69fa2f4ec59f951fabf8ad79cc48dc4c415a45`  
		Last Modified: Mon, 10 Feb 2025 20:28:42 GMT  
		Size: 5.2 MB (5185371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4cf122f6ad2cf8bc40d582537f22160bcf1843ff9cbabd0b1e776c9dfd37bcf`  
		Last Modified: Mon, 10 Feb 2025 20:28:42 GMT  
		Size: 9.0 KB (9007 bytes)  
		MIME: application/vnd.in-toto+json
