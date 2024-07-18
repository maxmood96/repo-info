## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:08120412f56afbb6a9364616a58389767a6c9b85f88ad91e44755a6abcd434d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a97c9a14d9c31ccc10aea7d42819bf78157551d73677632f6d27d8fe0789eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228644084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b3efb7a6348d5e0e74e8aa08ba778a189c428e6850e0dc2a74264eeafd1ee8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:55 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Fri, 28 Jun 2024 00:19:56 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820fd71fd1566b3735d8a148a0f98b0cabeda2e745e73c880fb50e9eee23f29a`  
		Last Modified: Thu, 18 Jul 2024 00:56:32 GMT  
		Size: 166.0 MB (165997446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b2cf593460086a7074aae451db47faeb3dc1c886bcc3b1b6f53dfa23efc57ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5975805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4804e0770dac8403e220c70cc95d9b5225c50732f93d07477fd0bd32ca8e3936`

```dockerfile
```

-	Layers:
	-	`sha256:20deff81aad5b590e18ea7305fd4f6f9064775e570c4f1924847506da7015080`  
		Last Modified: Thu, 18 Jul 2024 00:56:30 GMT  
		Size: 6.0 MB (5966088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:185df41e4829dec089645bd5b6c726cd4f44dc2b189466b4f0758b8fcde4b999`  
		Last Modified: Thu, 18 Jul 2024 00:56:30 GMT  
		Size: 9.7 KB (9717 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8db52261c75750bf40dd7b8d614b3c6a98561b865cdf31cb4391316e2d3a6671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221175539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c042a925a449f43f3c9160e70a96cdfb6e933abfa9d2b006327ee57fa3152a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:40:02 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Fri, 28 Jun 2024 00:40:03 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf8362c047485868752dfbf47ffa2441f516f3bde6e41c198c0e424eb08e76`  
		Last Modified: Thu, 18 Jul 2024 01:15:44 GMT  
		Size: 156.6 MB (156606774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cc4ec3f52d1b2a3f481a22f19dacb18c9e7c5fa7892e84ee7bfc41494d2fcd6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5767612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6947a9a19fa134b5614e1f33705fbdd959b9b48c0f870096e5af1d6fe0a6c88d`

```dockerfile
```

-	Layers:
	-	`sha256:a6a861042525279935f8d5fdd019633c14379fb669596f60e4404835e1d9999e`  
		Last Modified: Thu, 18 Jul 2024 01:15:40 GMT  
		Size: 5.8 MB (5757617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a8fa5e3e30652ec0987f70ab86d4417472a174f9ffebc030357a6404285847`  
		Last Modified: Thu, 18 Jul 2024 01:15:40 GMT  
		Size: 10.0 KB (9995 bytes)  
		MIME: application/vnd.in-toto+json
