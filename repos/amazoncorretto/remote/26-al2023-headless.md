## `amazoncorretto:26-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b46dec9faf057ff7adb1479a557cfc8cf9e67be3a1221c0f5dc06f2483e5dfff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:84ea652a5c3637c2d90e0a2b5e325b06d67363c7fe7aff6bd27bbe58113d0747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160396692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a410b8fd47db266eb765134a231c59542561063d94d5835da3898cb7c8e892`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:52 GMT
ARG version=26.0.0.35-2
# Wed, 15 Apr 2026 21:26:52 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:52 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:52 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb105f6b91ec86665df329f13f295f897be5855fc95ecfca82b225d8bd97ed1f`  
		Last Modified: Wed, 15 Apr 2026 21:27:11 GMT  
		Size: 105.8 MB (105825438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a6b34b9cc2801f0a023fe77f08b623e72f8952a980209bb7104c958636c8650a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd53da773d11c160f6784e52ac44833efc7d4327c7df9d7e17f54defc6544f8`

```dockerfile
```

-	Layers:
	-	`sha256:c3a9e8fe5867ac7363692453a7543656a7c0ce6981755d8dd87c1cdaf4d87ee6`  
		Last Modified: Wed, 15 Apr 2026 21:27:08 GMT  
		Size: 5.2 MB (5200404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc7a452122a7e04e173f12fada92695cb0a961bde77d1a6d584e466cfadfb6c8`  
		Last Modified: Wed, 15 Apr 2026 21:27:08 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c1ea91f44f384fff37cae75949ef03a32561e6c92048776464445a2396971c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158150678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28aa0c341ddae6285c07f50b5219ed684a1a00829f6407445c8b91a4687c79e1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:57 GMT
ARG version=26.0.0.35-2
# Wed, 15 Apr 2026 21:39:57 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:57 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:57 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0465855d982540409f8413f9f8a345531e474baa200da3a224a222cfcec117`  
		Last Modified: Wed, 15 Apr 2026 21:40:18 GMT  
		Size: 104.7 MB (104707939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:97c1956f262c797765fce09d65bdb7a371cb11096fa7612e93444e09972506a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7386425c8c8b4c6417e26bc82930193c05ef1883431b58f6c1099fa55b1c213b`

```dockerfile
```

-	Layers:
	-	`sha256:a7461e2ebeb316b214ab7822f86bcf7d22c1cb27978a3e146c0ece83988cb65d`  
		Last Modified: Wed, 15 Apr 2026 21:40:15 GMT  
		Size: 5.2 MB (5199214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d1d0fd483d30e0765e1ea87f6c37ebf9908c6799a14301aee1d178057988240`  
		Last Modified: Wed, 15 Apr 2026 21:40:15 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
