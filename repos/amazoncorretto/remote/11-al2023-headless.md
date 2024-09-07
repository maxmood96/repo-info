## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:e8a05e62e8556ed908cb9e9584576af0d414511f6c933b6d4c1920eec743c7a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8f3c9de351ddb7b89564baa10e76eab1e7c8f4c018ae0e77017f226793012447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128481650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9bc141370abfbc19a80fc8307614a41c8d2326d5a86897e973382f6cc3b4f2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f9dd052e142d6bbee3556a17548362b00b044603d859f7ff1a81d3ef6d64bd6e`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 52.3 MB (52325199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b26db9f957a36fdf937f8fd39af78284b14d3338c7d58e77fa7bbba520c67e`  
		Last Modified: Sat, 07 Sep 2024 01:05:51 GMT  
		Size: 76.2 MB (76156451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6c4bd459e959972b7b9174f084e11fafb9802080de0a6b18fdccdabd71d6c6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a99201fdf2f65fb1aa0d90d1dc0cb2f6fbd36e6cf0755e0b2f887325bb6c232`

```dockerfile
```

-	Layers:
	-	`sha256:2e496b59a61b99996e6810fa47d6929ff592b7fc1159274f23bb44640beffa54`  
		Last Modified: Sat, 07 Sep 2024 01:05:49 GMT  
		Size: 5.2 MB (5198499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:697306135d320da49c7238bed85517a4c1367211177c13f4ec83afae89044826`  
		Last Modified: Sat, 07 Sep 2024 01:05:49 GMT  
		Size: 8.6 KB (8618 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e2858325e7323700883f5c702df1f8a2cab80f824e79e5895d8214185597d706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126724264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b870deb4c6d59a13311e37c4fd9a32bf6d712016de3886a90b721398094a6818`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:875f26d62c6d0f5a935b0c8548e8375f2a9b98d7669bf434dcd5b36e2114348a`  
		Last Modified: Tue, 20 Aug 2024 01:54:55 GMT  
		Size: 51.4 MB (51426298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd814e880ce321502206a77c374545bac039a590667ed0b82243382d7adf0992`  
		Last Modified: Fri, 23 Aug 2024 02:21:27 GMT  
		Size: 75.3 MB (75297966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75626ccf8b39a274cbfc6a8ac546a9b4edc99673221b084bf42eaa381359f5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2ff81b0e2b58c4a52192418e9f2ac385ee25652351d629a8eceb72d4ae962e`

```dockerfile
```

-	Layers:
	-	`sha256:c751f60d8102cda926b794aff6790311e9fe1e7aa0a7f96223641ea76fb71db5`  
		Last Modified: Fri, 23 Aug 2024 02:21:25 GMT  
		Size: 5.2 MB (5198116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2df96e22457d3eff59073097ad902d6cc29b60450792d53c20fde59e5ac7740`  
		Last Modified: Fri, 23 Aug 2024 02:21:24 GMT  
		Size: 9.0 KB (8979 bytes)  
		MIME: application/vnd.in-toto+json
