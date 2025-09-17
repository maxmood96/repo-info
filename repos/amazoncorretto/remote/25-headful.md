## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:96f31da7af5a005fc11d70aa1f4c7ce96421a3e0e0d54fa87ce552f40f4309b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5cb4dd130b4fe61505f03350fde1b2c829c2f801cd73fdcc7421c860e32b3ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158190890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376e39a3e79f353854d0fb00f31cbe37f0188cf4081c206800bd258dafb79a39`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 20:25:28 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Sep 2025 20:25:28 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51acaf69dd3aee73823fdbfb15328729f50a3232bf58b44120017ccc5a4a41af`  
		Last Modified: Wed, 17 Sep 2025 17:28:11 GMT  
		Size: 104.3 MB (104315184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f90aa0a8449b820ed32a3fe200cbe0163fbf93c051f630ba6edf8b78a1f54eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780449f49862bbee5e5c4aa1c519b719d39989db60803acfe6dcfdfeb8d5644e`

```dockerfile
```

-	Layers:
	-	`sha256:b8a92ac642130ecdba22792bb790bf64eb52e016acf98c44d59dac9abed821df`  
		Last Modified: Wed, 17 Sep 2025 18:48:31 GMT  
		Size: 5.2 MB (5220130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e8f6b8ab713ca8a5d82e28948d51813409d77852d8c3a88c73b870ab1d05861`  
		Last Modified: Wed, 17 Sep 2025 18:48:32 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cc6c2fcf60ddc04240bef296b0639838c2357f1fede5b7d5fa6f63dec73ec52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156009082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2b3dd3b2e39969d269590fea9877dfe4e3c57e3056daf4dc89710b8dec7b19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Sep 2025 20:25:33 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Sep 2025 20:25:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a2133584a03a0323a461f4ba1900a168268d3305d6206a4e0a210c92b146e94a`  
		Last Modified: Wed, 10 Sep 2025 02:34:05 GMT  
		Size: 52.8 MB (52775111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132070c039937012df7f70faa8e32ad0fc1e99cf2ed946fdb51a3c8750d955b9`  
		Last Modified: Wed, 17 Sep 2025 17:28:12 GMT  
		Size: 103.2 MB (103233971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a96c68bd168486b0c5c2af23938fd731bcc053d7ceb020e2cb51af75b219b33d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d988dc6a55bd943e38867ab6c3530552572cfd0a060925a8f148e3ab89507630`

```dockerfile
```

-	Layers:
	-	`sha256:a6b87c6c04c86c5f3fee76454bdbe9f59340e6e73b29327a5d0b16efdad5f670`  
		Last Modified: Wed, 17 Sep 2025 18:48:37 GMT  
		Size: 5.2 MB (5218944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b423830fa9fbfe7c60f4045fed0800291a1b5730fc7ef6dbc3191e20ae11aac`  
		Last Modified: Wed, 17 Sep 2025 18:48:38 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.in-toto+json
