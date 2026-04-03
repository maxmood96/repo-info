## `amazoncorretto:26-headful`

```console
$ docker pull amazoncorretto@sha256:7634848758f35b513f2fc6f3280894eef83559f908bfe8af2bbf94f79cc95131
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:56c34204cf0849aad443e76c0a55acaac44e108b82db733c7bff29532dba34fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160572858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85990a22a5bf99920c4ce9db9f774eb2c4bc58ae0d73794030af72218b93f3b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:11:44 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 17:11:44 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:11:44 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:11:44 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:11:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc197f18953d55c220848d69980636733812af94d190bb5f1886fcb38d9328c5`  
		Last Modified: Fri, 03 Apr 2026 17:12:05 GMT  
		Size: 106.5 MB (106539768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c1c403f42c4032260d32e92948da8241c21a607fe11c2a0beafe15b14ffac72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc9cf28d604386e5d3a3f0d100a80176fa7d84af8b0198b76446f2e62fa54b9`

```dockerfile
```

-	Layers:
	-	`sha256:cea0a4b62af96571a6780d3a76f874a33ecdff453a63f43317a677434ad345cf`  
		Last Modified: Fri, 03 Apr 2026 17:12:03 GMT  
		Size: 5.2 MB (5219457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc1ef12a5e346cc771e96e8bf880e0451325f2548ed9cd73c88441a883b8e4cd`  
		Last Modified: Fri, 03 Apr 2026 17:12:02 GMT  
		Size: 9.4 KB (9369 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b3d275d1106e93318b515892ceab038fb3d2c3af316e9d0b3f1efb3c27421723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158374908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459a1b4220b0916a6d1fbde0e695ff031ae76c6b5fe45bd53997f1d1bbf9bbd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:19:42 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 17:19:42 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:19:42 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:19:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:19:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e4474eddb0012fa37e8436d896ae884d6b05d31918e33e5213e866918a96a3`  
		Last Modified: Fri, 03 Apr 2026 17:20:03 GMT  
		Size: 105.4 MB (105433533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0df437457d48d071c2c572b97293335fe98e0414895d57f3b4014f3530af4720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785372abbfa24129a8292d17b1ab2cae31786e1413e47252bb7e8b26cc900b5a`

```dockerfile
```

-	Layers:
	-	`sha256:34b014773f9c4b6f9123ebda347f650249daf3e065d713f0e26d5e1846833496`  
		Last Modified: Fri, 03 Apr 2026 17:20:01 GMT  
		Size: 5.2 MB (5218270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b720d57a7683682c217235e5a40ef3dd140b559a1a810a1a340d078664bae1b6`  
		Last Modified: Fri, 03 Apr 2026 17:20:01 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.in-toto+json
