## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b06457c390601ccf9c282defb12187e0484dbdeb0b03bc06332649af4cb743a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:811644e07f77d554ea0e79755765765e0ed0a96e5f8238739e465eb45195042d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157476298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ab6cbe77d769c5d6573ce44da2242fe4237d8eae6ac71f966e2a129857f7b3`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:d2c4495f6eafd283d5cb76033bd01c9a0ef6c2f98be6a3b579390259e40c515e`  
		Last Modified: Wed, 17 Sep 2025 17:27:53 GMT  
		Size: 103.6 MB (103600592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:206aebdfe4389a9884c6a8d729443994be0db27337f431b5fc9f8ce2d281b7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986da4c0ca232fc51654dd9c4022faff755316fbd1cd4d66e46778cf6792efa4`

```dockerfile
```

-	Layers:
	-	`sha256:a93d5ab94d0bc559a39f11829d2548f2b149225eb3fc2e59372f57923735294b`  
		Last Modified: Wed, 17 Sep 2025 18:48:42 GMT  
		Size: 5.2 MB (5194703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd77614be0a52ffae9ff916fd6cbf9f17636e2d7be885ce09d3eabd221e291c`  
		Last Modified: Wed, 17 Sep 2025 18:48:44 GMT  
		Size: 9.1 KB (9074 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:03f62884812c1d19ca1551930e82cedf7dd715770c8f85d1f9f847ddd9983ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.3 MB (155293402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b223ed95f92b46edc7c7fcdf348fa0fe75d4145fdd2427be5895f69637c844`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:0f1b4daaf78e838534756643f787ade317bc8e6d72616881203cce5129c2f436`  
		Last Modified: Wed, 17 Sep 2025 17:28:09 GMT  
		Size: 102.5 MB (102518291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:53622490a4d50728870939cbca24eb2809d1d113d080af68e48410cf2368793d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8912f976c54dbeabc2d8e0a718dd60e8a1b8a5482288245503aa28108e4e4a`

```dockerfile
```

-	Layers:
	-	`sha256:ca98cd9bb9b5bca1e98a3777561a2e1ee5bd245e7ddc644e5286a1a6709fcfb3`  
		Last Modified: Wed, 17 Sep 2025 18:48:49 GMT  
		Size: 5.2 MB (5193514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:981ad9ec4a48e8f7deb2365bcb5b1996a4dc2af5ddb6c6d68513d9d8ff82088a`  
		Last Modified: Wed, 17 Sep 2025 18:48:49 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
