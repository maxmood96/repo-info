## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:286625f1c729cf4ce68fc74f7f5f5beaa04554c384c93a3378a7a405b1a7a9fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c919766a1bb14e53de31ce4b75ebdb9a404c677add68bbe8aec57cf782cc78fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172078010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19d4b7770faf3b4c39d5d07facd8326bbee0382148c188f217f0f86af58a0e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:05:54 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 17:05:54 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:05:54 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:05:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1233d68e17f19d4cab9fb63a4bb4322316bfc6cacc9088e864b1d26319d3e009`  
		Last Modified: Fri, 03 Apr 2026 17:06:15 GMT  
		Size: 109.1 MB (109121500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:68d13857791c7329a021f055cf638ec24fa318d7cefbd31e10384717d6543741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be65f3fbbf35ecdfafe619936cfa880c5cd8923d745c9c1156442c3f9da800b0`

```dockerfile
```

-	Layers:
	-	`sha256:7a4c60ad0a4e61b1134d1c7205ebf4d5a496cfc4fd9f76af7910d9ce130f57dc`  
		Last Modified: Fri, 03 Apr 2026 17:06:12 GMT  
		Size: 7.5 MB (7504132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc92a92912daf33e12341d12ee6947edeeadbd7cd1f1ae6609ee2f4fb5aac33`  
		Last Modified: Fri, 03 Apr 2026 17:06:12 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6c315484b59a1b7eda747e0c3d0513e82be5c6f6744f36799083e59cdd06129d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117772189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb776fa2e70326dc06a0688a4176c616db69f07b1e72c73e9c0241965a12bd1b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:13:42 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 17:13:42 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 03 Apr 2026 17:13:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:13:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda7fa5f7b11f82890950b93e2e1bb54dd5812eadc8156b6d005706e9186b38d`  
		Last Modified: Fri, 03 Apr 2026 17:13:56 GMT  
		Size: 53.0 MB (52969040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fcfa1477b70f266ee4f27a74b18cf0a532a04f377222a88b1e02950d613f0049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d46f1f44d5b13fe0ded6238ddb92df6421d38dd24be2ce9f43753e0e28dbeec`

```dockerfile
```

-	Layers:
	-	`sha256:79d1ef65fb793ae3bebfdc5a1c5eaa0b408fe9e97dfdc64eb5328e9a0d886f7e`  
		Last Modified: Fri, 03 Apr 2026 17:13:55 GMT  
		Size: 5.6 MB (5618891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d80b6588666e87bb996491b2dfcae1fbc95b83a6a8fa40c31a980545ebf975e`  
		Last Modified: Fri, 03 Apr 2026 17:13:55 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
