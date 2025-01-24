## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:b7be7b3791e12ed551fafa56643839126e5a2cc33ae99fb47d17af5d068975e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b4a8e4569df727f140e2df924c0e96bd7acba0529587c2e9ffbf3971ec5cecdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153742592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63a9849e7a9027c2324651a82795f8516558a1d355bd6fbcba577489d8cb316`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 22:08:39 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 22:08:39 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2ddc0aa2636ed19b988b4176374929a92f5862f6c6e88ea255d352140af781e6`  
		Last Modified: Fri, 17 Jan 2025 20:13:56 GMT  
		Size: 62.6 MB (62648554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a256cabbc588d3aacf4c04869f87f456b5bbafcb50c8aaea81d1929f363ee5`  
		Last Modified: Thu, 23 Jan 2025 23:08:23 GMT  
		Size: 91.1 MB (91094038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a560d1540dd6717a3c95e35c3903ae889cef63f818d4d32b41ec70ca1be957b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5859023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc5d3dcbd4f2611e853d2e9d39139b8afde4871385c0ca3a9e1cdf8a8ca1242`

```dockerfile
```

-	Layers:
	-	`sha256:640c37daa4c7aa3d099f08d2f189527b841af5deb8d3cc2df732cb77a30a91d6`  
		Last Modified: Thu, 23 Jan 2025 23:08:21 GMT  
		Size: 5.8 MB (5849552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d451966b5d38e8c9ba2d74dc030ecc7a9d9650e0b0838a3355897b7544ffd75c`  
		Last Modified: Thu, 23 Jan 2025 23:08:21 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9bf888252172a614231a9ddf2978c939b7ecb1a711474d5155daf5e6ffd9ea51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146453332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5815b0b8094d47eef70df8fe214e6af5f036860a538bbcd72dc0e5b6a189367c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 22:08:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 22:08:43 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:dc3d403853487343f06bffefe21e65d842f88da2d7a1073ba2820fdb1b7ece72`  
		Last Modified: Fri, 17 Jan 2025 20:14:11 GMT  
		Size: 64.6 MB (64590432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd645deeb328196545a60a8d6960621be8375f03620c12d6ac4c1792246f5ec`  
		Last Modified: Thu, 23 Jan 2025 23:20:43 GMT  
		Size: 81.9 MB (81862900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:89e3f53b72399be9182017acdd47194e6cb52724b3017a65f80e883485de4162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5650846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689c672bc74ec1e8d4ff24a019729494459d99dfb2bde55a7f876307bc9ad428`

```dockerfile
```

-	Layers:
	-	`sha256:5f094668ffa5dcccc95f75792788058228c338d77ec3e4236e6eddaa22e38580`  
		Last Modified: Thu, 23 Jan 2025 23:20:41 GMT  
		Size: 5.6 MB (5641295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8244b9472975473fd48f2754280692c8b69dea7271efa4fbdddc1023a71df817`  
		Last Modified: Thu, 23 Jan 2025 23:20:41 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json
