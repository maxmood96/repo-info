## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:a3f872ffaa088f3bdc7d7183853b0cf487ae62e9b64ef3e84dcaf09c49097f28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:60a73e6e0fabd1b027419f8c9bf647c2261903f84a1ca849f2a08f92a32b5ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137782781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1385d7bee820315b8263cccff337ab015eec548c978e0e18f1d2ddd80595ede`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:30 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:15:30 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:15:30 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:15:30 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfdf8bd85cc499ee9e3cd69ea7eab116b8cc8c251df8eb543f6fe896bd0610d`  
		Last Modified: Tue, 16 Jun 2026 01:15:50 GMT  
		Size: 83.2 MB (83211625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4cc196c6ec649f5cf8b54e990d6366a0fc10fd273568ffbb99cc85283fb1091f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fefaa51e451623a0d3b7d49a9fb4ae2956ee636b137f4aa4c9a470d44c30359`

```dockerfile
```

-	Layers:
	-	`sha256:df91e066a10497f9ad06e87b38f0ee1562b6c8f357b8fee5e8234e43e00fd228`  
		Last Modified: Tue, 16 Jun 2026 01:15:48 GMT  
		Size: 5.2 MB (5215594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db97cb3ac8bd82577298fe028847991ae6750a5ae3d4c9581ba748fd63c044b`  
		Last Modified: Tue, 16 Jun 2026 01:15:48 GMT  
		Size: 9.1 KB (9053 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:32eb6d6d69b7ab5ee8b5776548665750cf64288400059c9845753d852dc7dd97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136093006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783a61c8c8f28d5324c48502025b725227a9d24b69f5fd7f8de96339576f2afe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:38 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:16:38 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:38 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:38 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180b458ccd64d82a63d607de9cbf3a0baa21892a5bf6337652a29c9a2ca99cd8`  
		Last Modified: Tue, 16 Jun 2026 01:16:57 GMT  
		Size: 82.6 MB (82635179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:867a27569a08c526cea62af2a786ca657e66c65e6625240180efe77b3daacbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4820fc805e15f87332f13f513fa700b51e247e02cf597eb7014958a2413d5318`

```dockerfile
```

-	Layers:
	-	`sha256:23894fa1faa1587d39114533e99646a7ef99741d83e0a7f7f70f6a1bcce16a8f`  
		Last Modified: Tue, 16 Jun 2026 01:16:55 GMT  
		Size: 5.2 MB (5214386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d372a13322b52fc3eb6fdc4a265eba0b1e91a925b4be22e35b0af51eeeccce6`  
		Last Modified: Tue, 16 Jun 2026 01:16:55 GMT  
		Size: 9.1 KB (9132 bytes)  
		MIME: application/vnd.in-toto+json
