## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:83d225f44b15fad3fa92c8617fd658cea069ace60ad6343c419dda5ea5129f97
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
$ docker pull amazoncorretto@sha256:36cc6ef3ff6dc87c5b0ac61e55ed124f7dd37acf7ec504f67ebce3c3e00ea911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126723680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727d534d8536d9edf25c65f1c111cbd451c53857a96a65f21df135efdf79893e`
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
	-	`sha256:5df0cce0a70b576e00cfe75d45089073c37754f2920c4a7a79f3ed6e6500982d`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 51.4 MB (51426143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f77560140e7207cbad438796e9c897b69f5ecafbc80a025fa66b024fa52f8f`  
		Last Modified: Sat, 07 Sep 2024 13:14:07 GMT  
		Size: 75.3 MB (75297537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a65307f0a4b541758ace672b319897f25b8d5a57d4566f5e84072dc7cffe4981
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30a98da742a4458a8a78e8da32894944f937508fb620d01ab47a22e8487e565`

```dockerfile
```

-	Layers:
	-	`sha256:543af3872b6af9f9606da3734b277f1727927266c13b7a9b32d5e46e826c472d`  
		Last Modified: Sat, 07 Sep 2024 13:14:05 GMT  
		Size: 5.2 MB (5198116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9c5f8bc52b711234698a7a8fc58df6ad66b351bb661c6d09814b02ca60af44`  
		Last Modified: Sat, 07 Sep 2024 13:14:04 GMT  
		Size: 9.0 KB (8979 bytes)  
		MIME: application/vnd.in-toto+json
