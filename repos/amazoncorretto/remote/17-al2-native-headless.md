## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:fa562a8821e547d77eb95328025cb51661fd866f11d3a8385ac65fa494dc628d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:aa4c69eb48bf689d501d6fc9f1708f7e937229d1d4571c31cc32c6141966e628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150502069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80577fc4e95e4ea752419b7d08dea7e645112230c9ea5356a84df99ec92bc055`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e85e194f482efd491d25462c7e0280d2a5e0c26afd224a5525b468f9d0e8f53`  
		Last Modified: Mon, 06 Oct 2025 21:12:25 GMT  
		Size: 87.6 MB (87561449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a749cde5ffe29a9d19209d18219f8cca594533e63c0eb906b5bde5c527628a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4984505c45daeb5a02fcf1ef1f980dcce58829e1dc48ccd81733cc749d002`

```dockerfile
```

-	Layers:
	-	`sha256:40fca7e127463082f1e487f6176687e40e2984a4cab30c55510b0386f413bbc0`  
		Last Modified: Tue, 07 Oct 2025 00:48:53 GMT  
		Size: 5.6 MB (5631755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46534c716842159a43d3808873ab5b5441c8d14edfaadb7bd3fd5e62d7d2ce0b`  
		Last Modified: Tue, 07 Oct 2025 00:48:54 GMT  
		Size: 9.3 KB (9336 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1b6578c3446359fd69d15f9144ef513a61c54d228b4682df78b82110fcbdc188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144581968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d472f8a377ae3b5b08e66e79c42a88c62dba4e79c91ef26669276b71e12234`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f72ee36eb67b69a406cd510003debe0f9e166e68e516acadfc3a715989bf88a`  
		Last Modified: Mon, 06 Oct 2025 21:13:09 GMT  
		Size: 79.8 MB (79788760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d5276e29d70f9b904dcaf4a46bb373f1aea9927896a8becfba0a2142b2f48665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf9d45ae92f47407c9abb59b6bbfc3c98f3e3af1e8c98b3fda456e928416a18`

```dockerfile
```

-	Layers:
	-	`sha256:37f74d028a28df818cd0cdd7371590b4ae9f6a237aae9883d5a9ea1a7c91b6ce`  
		Last Modified: Tue, 07 Oct 2025 00:49:00 GMT  
		Size: 5.4 MB (5448031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45b1bf7f1c6195c5693c2775f6141cbc16352a6a36395247bdb116eaaa04422`  
		Last Modified: Tue, 07 Oct 2025 00:49:00 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json
