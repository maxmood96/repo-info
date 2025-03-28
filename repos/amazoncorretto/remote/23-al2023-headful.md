## `amazoncorretto:23-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:e928092cd462500cc0908e89a755b0c6cfd7ae1cc683b047aac2105fd4e32058
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e5659a43981228c56261774e85c9db049050ee79f8f9dbfacd13caee9bcc6fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146979793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14e857a9495e9ebe9104ac947b054b7fc31e7f9bffe79f53d08dcc150957b20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=23.0.2.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9e5e7840179d1503fc02e709068963f430690d59da2f720d2319effa0ffcb8`  
		Last Modified: Thu, 27 Mar 2025 23:58:49 GMT  
		Size: 93.9 MB (93856504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de383246184d282e8e12903a269423f74907a6e73fa906a3c6efe4c9a4ce9014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ced0ceede1f1cebe3aa56775c3db765dfa2ad68bad06c4c4b2a81937c00d9bb`

```dockerfile
```

-	Layers:
	-	`sha256:9661afc6835ab543d97316878a0fb6ace996930d3309fce71c5bfbcf10d85bf7`  
		Last Modified: Thu, 27 Mar 2025 23:58:48 GMT  
		Size: 5.2 MB (5189400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d1f02efbac7858f6b6055e7bb12c4c058816eb560f97959114245fb9882526`  
		Last Modified: Thu, 27 Mar 2025 23:58:48 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c5399b6a3b8da1dfacdac1d774e2f8f2ea3dbdd41251dd2056689926a6764ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145121548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89ea87d3b3c48f388f95ec569784ad8b6ee7e15bac1ec9c6d4af9b13dde712c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96009f08663f7e435c415b2ab3ebad5b723e4489edfe5cc4664b97093c3443a1`  
		Last Modified: Fri, 14 Mar 2025 00:31:38 GMT  
		Size: 92.9 MB (92875570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8fe39312309f72b5843b8a9c91391949192e3717d76f4fcc5268b8d7c4be2203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bccc77080fc12fbb6e89866d3fb6d91f82711068170ed2c334013dc0e53b45`

```dockerfile
```

-	Layers:
	-	`sha256:f13661ad5df0ac145b359f7b9c0ddf5f492282d35d502cc22781d3816a522b40`  
		Last Modified: Fri, 14 Mar 2025 00:31:36 GMT  
		Size: 5.2 MB (5187392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2fd4fa7b7ac1f936c8f3c59c2e8870a2d03faed95b271410b019f1ccd7f148`  
		Last Modified: Fri, 14 Mar 2025 00:31:35 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
