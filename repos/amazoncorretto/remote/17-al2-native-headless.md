## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:bcae760e67e16d9293e36e6f488368342b900a6383c8bd031a79b0e12595c41a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:26c9f3c53c779b326a80d02e59d59c5337ab04eefb7abd61ed8a45911e50c505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150556685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e55330cc8ca3a622c17cc906d7421255198c915e415c5a1d19c0c74c9c2ff13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5012a5ce7468c4961a47d20f25513ce52f8032805e87ddf03e9dab4f244845f1`  
		Last Modified: Tue, 21 Oct 2025 23:27:47 GMT  
		Size: 87.6 MB (87616065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8e37d6a57aa5c0c8890e8b3fb2ed14d5b0a7eced517aa50b7cafd5a83a549eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd558bbaab0c6227611cb7fed468f1960f16e53ed5788652e52e0fd83cb8b929`

```dockerfile
```

-	Layers:
	-	`sha256:d17c5bf41e8440df366d8fa762b20f1fa1cd9510a4c4aec84573cca935830709`  
		Last Modified: Wed, 22 Oct 2025 00:49:41 GMT  
		Size: 5.6 MB (5631759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cbe8493b07eba060ae6d46e52f551f9551a286281643260b82d6cb081cb4873`  
		Last Modified: Wed, 22 Oct 2025 00:49:42 GMT  
		Size: 9.3 KB (9336 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5d7539323259107bcbe2788081f0bba05cd3da62fb21b428ca20844e2ae7a6c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144622803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ed809d861707b890ba565776ab57a78d238239698f2413b9989077a362e414`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78391f15061e24aa4b841c24a0b1e54d861bc681f7126de6835fe371ac0b220`  
		Last Modified: Tue, 21 Oct 2025 21:50:35 GMT  
		Size: 79.8 MB (79829595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7bb0376fd234df85c395e6524f74408fa68e39776aba687f9739474deb0d7daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbfa59ef5583249936ed48300f394a45fcc9fbb4b641837b90e2e7890bb4b11`

```dockerfile
```

-	Layers:
	-	`sha256:deb6910e9e572e39c012dd4b039042ef7152b872363e9154d9f744564f3c133a`  
		Last Modified: Wed, 22 Oct 2025 00:49:48 GMT  
		Size: 5.4 MB (5448035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c2d5b7221561ab843c14d784210d6aa2dfdcf7febe0574fd2ad17b2f620dc7`  
		Last Modified: Wed, 22 Oct 2025 00:49:48 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json
