## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c46e726ffafada595803da4eabeb32694369c90ae1fa07e9e164136da13b6435
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:44e219fd291a4f0e272736a14244f346606941e78d6308a3f185d89573603a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142840606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da30fa79d44261aad21e013bdbaf40002fd2f6a914b9cc3e0e85839e8792c7a9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebd622c999b311ba2d8163de2de821f4e4de82a22b81ed1e4ebc2006468ded8`  
		Last Modified: Thu, 23 Jan 2025 23:08:23 GMT  
		Size: 89.7 MB (89688071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:281dcf20b137f9ae2cb3663a9c1cc8a5e70da43d51ac876347b7b1b3786e6266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede085b53d80aef1ca3b2202a25eda842a2c1daa6387924b691c0cf0564dff9e`

```dockerfile
```

-	Layers:
	-	`sha256:e92ae51d583e3407a8e44d406c32eb8a9db83d72504bb5839a4697e7f2a130e0`  
		Last Modified: Thu, 23 Jan 2025 23:08:21 GMT  
		Size: 5.2 MB (5206286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6970890b8fa5d0b3feb781b811252158577f1671657745f6dca8e3bc733b038`  
		Last Modified: Thu, 23 Jan 2025 23:08:20 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6e2cab382fe6fe2d68fca1304bbabd8f40e9d66174511bcf113cecbfd75bbc17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141105944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b976aa74b37cdec3f4b91fff8e8e66724e22df1991255df5ee63997b94b3aee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25baae0999f0c1134537de40a50bb42fa00a23c2e88e7b8b51d2057a4dfda3`  
		Last Modified: Thu, 23 Jan 2025 23:25:16 GMT  
		Size: 88.8 MB (88835745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c5f269ecbab28dfaca600374c15edeee85a53290dc701bcbdc17d6c8138def8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd675ee0f146456a0750183822ddb0f07d0ecb6932bead32ce51ec25dcdcb32`

```dockerfile
```

-	Layers:
	-	`sha256:7f1716e1bb3533d6b58114fb7f5f3731e76da30187e31b557f07bdabcf964a22`  
		Last Modified: Thu, 23 Jan 2025 23:25:14 GMT  
		Size: 5.2 MB (5205079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32074fd9166729afff674ca4e01df1ce7c88c8291ef295fddd91cb05601e0fc9`  
		Last Modified: Thu, 23 Jan 2025 23:25:13 GMT  
		Size: 9.0 KB (9007 bytes)  
		MIME: application/vnd.in-toto+json
