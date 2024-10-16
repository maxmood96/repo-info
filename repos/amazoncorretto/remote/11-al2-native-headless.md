## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:9768eb4cc5814c113e7033fb5a95f3633ed6fbefd17eb1007be83bcb8e8f7c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b14bbcd2a30491798780d3765f01ab825b4e30977f83611d967b25ebd171c72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217568240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b54b2a813c8a9be2070a77fce9f14ba84d8748d05a26d6bdceb2ade3983132`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:55 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccbd846c51cc8f69edad16410551fddfd2dac6a6807073d632bbe42a7a4b1da`  
		Last Modified: Wed, 16 Oct 2024 17:56:40 GMT  
		Size: 154.9 MB (154890084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ddf0708ea038c1ced9d5c1fb4ece6f39a1fe463989d1ba04704eafbedd77df14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5688106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2cbc04762362398f749bf1cba8240296054538e6f907e2ee3b334359ad1dd1`

```dockerfile
```

-	Layers:
	-	`sha256:27ab50adb44b48c722e21371a553132df984a9b145d86615a153b621324fcbca`  
		Last Modified: Wed, 16 Oct 2024 17:56:37 GMT  
		Size: 5.7 MB (5678771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea362c531777fc426eb4d0510e727094c17942a46218c0b09a6ec25bdd538bd2`  
		Last Modified: Wed, 16 Oct 2024 17:56:37 GMT  
		Size: 9.3 KB (9335 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c1523b492b6c78f738071dd74eb83eef9012f076b0725ec79902426ca07a5e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211828059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2f8c8b2e85e281fbc0edf40a1c2f7900ca744b37646f267d4501c0a584cfd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:59 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f90876c714e2f67a5510bee7ac869f190171cd16e46fe436d30cdf5f2da7ba0`  
		Last Modified: Wed, 16 Oct 2024 18:15:36 GMT  
		Size: 147.2 MB (147235400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f48c1382478ef298617f5dd7e2307d536b034d3336459707ee7d95cb78a1f281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5506356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d795bc30c91fe46622f1d3eeab47af5fde71b4c97a519dc0cbdb084e27bc38`

```dockerfile
```

-	Layers:
	-	`sha256:5996058d8a394aad8edaba6ce10a546b28baff9e3cdced12668e8dd68a2de8d9`  
		Last Modified: Wed, 16 Oct 2024 18:15:32 GMT  
		Size: 5.5 MB (5496942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5b5846ad2f9dcb6545ef7e2b7abf1ff721be14daf392f44c664bedb30e12ed6`  
		Last Modified: Wed, 16 Oct 2024 18:15:31 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
