## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:9e9730d67c78523fca2f0798eb5a0c68f259da8507129fc06ce485ac01d0d61c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:686f1a30aaf60a39edeebf8ee8132ce87d411ff0ac7bc6ea68907e2325f9524d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150376416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432838520637647cc70155ded777fdec8a3fe55339207afa04fda67fd2b1a850`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeef74e01ab71f7e99a8a2f7636d36f003ca4a7222bb68d7ece1878ea9147a56`  
		Last Modified: Fri, 05 Jul 2024 19:56:47 GMT  
		Size: 87.7 MB (87729778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bd60a4a4c9f4f52a7e81550b2abba3ea1e771aff29ce5d2b7e7b9a97bd44016f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6708bafa3b727076b3a31bc090229afa6787d738e00f0a3c7386be87eb2619d2`

```dockerfile
```

-	Layers:
	-	`sha256:edd2767fb659191746af8dc490dc44b45f60c2c28b1b574722a794bca3df6932`  
		Last Modified: Fri, 05 Jul 2024 19:56:45 GMT  
		Size: 5.6 MB (5602702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104f4fd8f6cf5a7c5ed64b75ff6c4d1e80e8dcabfcd9926ad275654c52823bee`  
		Last Modified: Fri, 05 Jul 2024 19:56:44 GMT  
		Size: 9.1 KB (9097 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:db31e4668651513d0fff3b3ead415c98ce57d2ffd760b109ae03fa7771678ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144620222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ad05cdeb6f0729e1c51c8db7b758bf5326cacfee05358e3f4f009aebce68be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=17.0.11.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e0e933fdd99479436842f40d94b0b7799bf752234611e763a5a0af1aa1ecb8`  
		Last Modified: Fri, 05 Jul 2024 20:14:57 GMT  
		Size: 80.1 MB (80051457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:99e5d56c45a8262322f27daf2c6c63d03a599b3ab0697bc6b42305c8d8f40f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5428051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b695f99ae7eacf113334c731d491481c979d5a0d25a592287da79941fe740c`

```dockerfile
```

-	Layers:
	-	`sha256:172072935354107840371bd24f9b73487a8b4a79e15fb5b19120e24f46823ae4`  
		Last Modified: Fri, 05 Jul 2024 20:14:55 GMT  
		Size: 5.4 MB (5418676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e186dbd116108e046a0b90d1f4b0329eb48ad0b784ec5ecbfa531253807bd711`  
		Last Modified: Fri, 05 Jul 2024 20:14:54 GMT  
		Size: 9.4 KB (9375 bytes)  
		MIME: application/vnd.in-toto+json
