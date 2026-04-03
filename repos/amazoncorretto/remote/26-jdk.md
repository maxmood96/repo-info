## `amazoncorretto:26-jdk`

```console
$ docker pull amazoncorretto@sha256:c6c2bd4cb41bea7d3435b59353c4a52cda1c30483373907c103dd606b110a843
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2e4b8afc2d5e298159dddff2e3e179689b8b0793326226ff2081a8d6f06b41e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247484208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d92ec21e207765f15cb74de24bfe11ce8d70692c008fb031c2943a82ee7a99e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:11:06 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 17:11:06 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:11:06 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:11:06 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:11:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a7fd721e84a3939237d83ac839e7cf140b067b149481941c35cb3490c5fecf`  
		Last Modified: Fri, 03 Apr 2026 17:11:29 GMT  
		Size: 193.5 MB (193451118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb70e1295d3fb0b98c1708bc5acdeb2f29e18d88cdcceaff37d558852a94a077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cac34422eef042c139dfa2ab32f9ec58a5893225983ddc5949597511b77f954`

```dockerfile
```

-	Layers:
	-	`sha256:39204c169240b96b42a3b165f9e6a6e267db0868dac23f7e14be2c22e7a3e491`  
		Last Modified: Fri, 03 Apr 2026 17:11:25 GMT  
		Size: 5.3 MB (5326370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e1b12646dabfef5d4cfec9e3c5ae5d4132c6beb4ef83faacd53a9334fa5465e`  
		Last Modified: Fri, 03 Apr 2026 17:11:25 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cba13a49ad743f368e10239454de3e9178e596789b10bdbe313c9701ca30ba29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244215577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32a113de0ec60a67d4ff7264076c9b3896f9079e41305cc714ed92624a48fa3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:18:42 GMT
ARG version=26.0.0.35-2
# Fri, 03 Apr 2026 17:18:42 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:18:42 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:18:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:18:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003572eacab35bec102b46c7d55a333a2d1f34e79f4b88c2745daa7785346fa3`  
		Last Modified: Fri, 03 Apr 2026 17:19:08 GMT  
		Size: 191.3 MB (191274202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:41c3bc49f488ee330714f9b2d3cd4d79b945007b98b4c4b2aac121fbfce13ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abed2854e060fe8643ef2aff32a1d59995263c1293690802b8fe35065fc5284`

```dockerfile
```

-	Layers:
	-	`sha256:801a77d2ba0532357dc72527328c92ded3d9df6ad9928a32f4584a5d2ddeed7f`  
		Last Modified: Fri, 03 Apr 2026 17:19:03 GMT  
		Size: 5.3 MB (5325346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea828b2d235b10a249243e525b8da3de2cf3096e6c9750e9f616f5f9e53abb54`  
		Last Modified: Fri, 03 Apr 2026 17:19:03 GMT  
		Size: 10.8 KB (10779 bytes)  
		MIME: application/vnd.in-toto+json
