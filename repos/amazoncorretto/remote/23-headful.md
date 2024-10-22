## `amazoncorretto:23-headful`

```console
$ docker pull amazoncorretto@sha256:0679eef2bc4b462d85a4b12bec4be3cab0e952ef96a265134850cdc71834aeeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8f450137590fe1f15060ba66749d11dbc59e39be2aff7ed1ea83ef40120d1872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146142448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7593bd07974119866335d1935e49bc61ccccd8f43f9f911051e52ab730bbbb13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26dcf92151ed7827c480bb70702ac6650c33b482a2353c1a9dcd44d39e7d7e3c`  
		Last Modified: Mon, 21 Oct 2024 18:57:14 GMT  
		Size: 93.8 MB (93798616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:552ac156fbbd9830758f7ac4c83cfbc5c69c83fd691347f7b161f92779923001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6469f86698aadd4e85a5769878c105dcb97b484d1ddd3837cbdf218d3e8d0a5b`

```dockerfile
```

-	Layers:
	-	`sha256:bbc0afe81c0b6500fc0343c9738a5d1dccd89701f204dbc2668ec0f4d0a5b02d`  
		Last Modified: Mon, 21 Oct 2024 18:57:12 GMT  
		Size: 5.2 MB (5214298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2869c20a6c312fe1cc376ba601fd36adb2097596476f86b235acd75f927bc78f`  
		Last Modified: Mon, 21 Oct 2024 18:57:12 GMT  
		Size: 9.2 KB (9248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:05ddb7f591a2b20c53f521eda11e7d3d07b5ae5f130dfc4e68688bfa80f1298f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144203581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b632915a840448dcc66f9229247ecf9215f995f830115228e00771f6030008c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:923a2071aa1c62af0f57aa46e86e64587ba93da0a38eaf52d228227154730e17`  
		Last Modified: Tue, 15 Oct 2024 02:53:59 GMT  
		Size: 51.4 MB (51424527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba59ee97ca38135dfa9c4c6196bca5dc076978c9881ed44903197a7b9edcc9`  
		Last Modified: Mon, 21 Oct 2024 21:08:29 GMT  
		Size: 92.8 MB (92779054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:617f698eb7f128241bb778b23e2fea184994c834b7217309fe0758163e2393c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2f20766df26a540709f2284238f7ddcb2bdefb7a6d479e243ca0d8c794734cd`

```dockerfile
```

-	Layers:
	-	`sha256:4c0aa0a11cd816cf52d0c348746ec70a2ed8a1902ae557e5144a5158ff8e7a38`  
		Last Modified: Mon, 21 Oct 2024 21:08:27 GMT  
		Size: 5.2 MB (5212287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e1aa48c015ff9d00767bb83ce425c183714e721349c9031d45f9c708540795`  
		Last Modified: Mon, 21 Oct 2024 21:08:27 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
