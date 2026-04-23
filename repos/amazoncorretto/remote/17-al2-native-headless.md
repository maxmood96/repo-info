## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:133af3cf6a83a67fc9864d07104d4147e70942cd2389994bbc76114adfdc1858
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:49fc25237eea87ad60856f30641c4e18dc3e54e7c2b3d629156f48f5a6361f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150666367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf26dc0d658f0cce5778f1f5dda049aedf428513e7b6c94e22731e3356211fc1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:19 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:19 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:34:19 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a9bb9897797b3ef4252f824cd0235a3a2b89a5bffb3d63bebe429526b34794`  
		Last Modified: Wed, 22 Apr 2026 21:34:37 GMT  
		Size: 87.7 MB (87711101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:37a41a1de3307ea8e0114f1a742aa4434ffb598768c784f28d13f25afda57cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5642142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95aceda662c19236803d16bd22a20f2f2c3a5f2d3504b98dcbb6015a649dbdec`

```dockerfile
```

-	Layers:
	-	`sha256:d938d44580b6737ca7ff3a90c11a885ad96a3eaec59b95af72e6ed0d8a0176cb`  
		Last Modified: Wed, 22 Apr 2026 21:34:35 GMT  
		Size: 5.6 MB (5632679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14605c22dac19ff3a8883d1a61acb026626aceb72d42f42e36f32ed7f11023c9`  
		Last Modified: Wed, 22 Apr 2026 21:34:35 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c93f197fd4aa78bd2f1ca976563eb56fb6d5c5f9932b77f2faf69f1ead1d1f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144741685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e6104011921645bb04b4224232a123484acc22a39422cc38d58452bd41db52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:13 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:13 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:34:13 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb7e063e4229a9218a836fd04e82b8db747a8a2465e68f59d6983b6e2d56bb7`  
		Last Modified: Wed, 22 Apr 2026 21:34:31 GMT  
		Size: 79.9 MB (79938710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a2f4c77fdbf90e80fdbe0dfb86585a1b2099211d909c89e7b3180ec9314d879b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd5e02ee74dede4511bbab4d588b301b3962101fe815f11d5f864254dca7f0f`

```dockerfile
```

-	Layers:
	-	`sha256:ea33297c2f64d39f209bfd979a5a82d2f4de5555b545528cc3c20fb947a5aa32`  
		Last Modified: Wed, 22 Apr 2026 21:34:30 GMT  
		Size: 5.4 MB (5448956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf73124144588f05edf109e8e2817c8f630381892cf1866c3e92cc2cd200f151`  
		Last Modified: Wed, 22 Apr 2026 21:34:29 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.in-toto+json
