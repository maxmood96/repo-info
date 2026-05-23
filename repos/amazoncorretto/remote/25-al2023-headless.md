## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:fdb4103ca7c7d88e0af7f3e3fc24e755518f1e95e8bc807eab6b88a6922dca33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4666651d8ed464da3482a29b147ebe988467440bb6e7b704938a81accea4248c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158293837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668b1827cbe24908556571db2f3845fe470d5e05984136bbc2cb9938b2210e9d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:35 GMT
ARG version=25.0.3.9-1
# Fri, 22 May 2026 21:12:35 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:35 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:35 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4981afc16bca9f6a8d10581f16f7987aca0495e0ca762031bac743a6f9cdf2c8`  
		Last Modified: Fri, 22 May 2026 21:12:57 GMT  
		Size: 103.7 MB (103721397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:266a0d34c664abc3c037a61c36ff6bd52ebc5fc82fd55b55e095c7994de254cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e16c57bcf2a694bff65326ebf0f44492a102162f14cbbd1ff603c8d0c57ea82`

```dockerfile
```

-	Layers:
	-	`sha256:afae002eec4e64caefe077210e1086860ce0712b07f360950abca39c630a5fb7`  
		Last Modified: Fri, 22 May 2026 21:12:53 GMT  
		Size: 5.2 MB (5202050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f997e030858db479944c9cfd75ec13bbe3bef8c3fce3205e22307d5e20c1dd43`  
		Last Modified: Fri, 22 May 2026 21:12:53 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f82d8b7ab14a48bdf934430829a6dcbf452741654e1557b6e3bf2d876ce0cc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156106772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0bc150d1e84deceef351cd273e38aa64dab9cf30efa1f6e81faf4649e43813`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:18 GMT
ARG version=25.0.3.9-1
# Fri, 22 May 2026 21:12:18 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:18 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:18 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5d22c07a4fae530985b4e013b7cafe4019aad1892cde1dfcc212c46ed89e85`  
		Last Modified: Fri, 22 May 2026 21:12:38 GMT  
		Size: 102.7 MB (102652357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9629840738c14ad346c53771e1dff2ea2239357cd97257bad270f651e77dc114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ce5333843920982065221b013818d91ef829ff1ef1b89282fb71984b333592`

```dockerfile
```

-	Layers:
	-	`sha256:8d8bc3ebba5fc27631edad2dc9d2efa4493564cc1fc57d3a34e1c8592d1f666e`  
		Last Modified: Fri, 22 May 2026 21:12:36 GMT  
		Size: 5.2 MB (5200862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788915e03dd3aff3d33370d2b27092eeee3a700a68fa90d633498a7fa4f3c889`  
		Last Modified: Fri, 22 May 2026 21:12:36 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
