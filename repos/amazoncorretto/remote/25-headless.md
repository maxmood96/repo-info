## `amazoncorretto:25-headless`

```console
$ docker pull amazoncorretto@sha256:9cb53fc50194a05c67dbc81e8d131bc23dce45ae5088bcaea6674ef90cd8e5c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eb5ed8ddd1da5b6eca0679fef373f1139481eb9662a9cbb364c611c7b074e2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158298132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23ac7745d6aaf684d55ebabe591b53e7066762c93d4567e25f928e8bb4bfb9f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:06 GMT
ARG version=25.0.3.9-1
# Mon, 04 May 2026 20:13:06 GMT
ARG package_version=1
# Mon, 04 May 2026 20:13:06 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:13:06 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:13:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae0c74aee96848a2c973c57c67fa3d003d294f959cece8d965de6019be37c2a`  
		Last Modified: Mon, 04 May 2026 20:13:27 GMT  
		Size: 103.7 MB (103721379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:57f375f281866b8b641c3f8182c740825953724dcaf82f11eb12791d2643d1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcb63ce509497111d619ec40894cf7ca2498276056eadd4d090bde0aa5366d9`

```dockerfile
```

-	Layers:
	-	`sha256:ba714eab6d8835cedc07318f4933063ac8b73cc27f0f4eba52871f5432a5ccb0`  
		Last Modified: Mon, 04 May 2026 20:13:23 GMT  
		Size: 5.2 MB (5202050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8229f57f513117efabeb4aba7f05a9f7066d2d9f4fd8e5f767602c91196c2299`  
		Last Modified: Mon, 04 May 2026 20:13:23 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3b3a8f4bf7e29c1a39b3fdc811289e96ef11efa4196bcae42082ff2cfc07ae4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156107738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e4fe79133e951d1dcb89bf8d3e6a7486ca1a0fb1da58504b11035d843d6a17`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:39 GMT
ARG version=25.0.3.9-1
# Mon, 04 May 2026 20:12:39 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:39 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:39 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94057c9cb5c9fc876399160e9064db938dba0c8d3f19d2847a9c1f1f3bc062ac`  
		Last Modified: Mon, 04 May 2026 20:12:59 GMT  
		Size: 102.7 MB (102650968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:24091e84064bbcde36c98598ad596414b418814c64dfd288ed768778dad976df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e08a8fc15918244e7758baae7799a8a4d940e77f95bcd09e421fb0d8ff2104`

```dockerfile
```

-	Layers:
	-	`sha256:a1eef278a244bbb68130ddd93d7ba65f7c79846870945884eb4c9d21d351b6bf`  
		Last Modified: Mon, 04 May 2026 20:12:57 GMT  
		Size: 5.2 MB (5200862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:528fc881fb988c3007e7833d9fb7993bd25d17e9c913827a7e09008ea0ec6909`  
		Last Modified: Mon, 04 May 2026 20:12:57 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
