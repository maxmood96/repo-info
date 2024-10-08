## `amazoncorretto:23-jdk`

```console
$ docker pull amazoncorretto@sha256:0db2829a03d3671507f6d999b84a3298ed64c31e22312720ff4a8c9f28695cd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:787945a39d1fb9deba4c54b72c253f0d5845873de1ab480ae2c13bcecc26af57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229783826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a441310b107d380b42a6260c461a774dbb036649ea9a394b0170222d98465f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e3f9dd3ef111133957f43f8599c13df571d514698c8206ae87e158071bb7f2`  
		Last Modified: Tue, 08 Oct 2024 00:01:12 GMT  
		Size: 177.5 MB (177458521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:884abfc6f23973410cd9ed336847b42e7bdc388ed887c89eaba2f906bf61414b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5331786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab9583924fda6f397d34cbdda4447773dc9df9f64d63996ad3dce0f0ff4e670`

```dockerfile
```

-	Layers:
	-	`sha256:5bd81c671474612f3db06c4d8176cd95855d5a74d0c368111404346e34a3669b`  
		Last Modified: Tue, 08 Oct 2024 00:01:10 GMT  
		Size: 5.3 MB (5321577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91fe69611583ef01c89aa6c6230cd8d7a615574d9ce060d0c2c41592fbc2415a`  
		Last Modified: Tue, 08 Oct 2024 00:01:10 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9f1f4f32ffcfa974d1652249507b33061a19b96ea982f6d40403a438a92402fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226816018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f035552517ca67a098221d09c5e2aaede9efa752ebf8e8d14abfef673b63f335`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd75179d52dd7e8d4ae0c95b646c4e8c091c51114cbbd826123391261ca3e77`  
		Last Modified: Tue, 24 Sep 2024 02:49:10 GMT  
		Size: 175.4 MB (175390026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f69781c73d9304455786f89630e23f46730a8bf5b3fa1caf459ac101e1a7e816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d6ca28886d8db27931e03d4e9ed92cf688e1a18f8c01ebf9bff9d136cc846c`

```dockerfile
```

-	Layers:
	-	`sha256:da36148e4431ce484a0dde08770b89a143c3dbc8bbb760eb4eb9553a779afd04`  
		Last Modified: Tue, 24 Sep 2024 02:49:06 GMT  
		Size: 5.3 MB (5319705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8e4e9510a9db5fb54ab1e8c86d4eeb5b50dd5c640d7a479fd241baed064488`  
		Last Modified: Tue, 24 Sep 2024 02:49:06 GMT  
		Size: 10.6 KB (10602 bytes)  
		MIME: application/vnd.in-toto+json
