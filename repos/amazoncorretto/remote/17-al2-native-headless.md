## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:773cdbd5b3f878c4925da0df12799a483f2248821e128ef75c838a9c8e885515
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a29e9932948a8d181ba1f4a70773c1dd1463fdc3a7cb66ce47cfe6da23bebc90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150552777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c055ce9683dcb545ef32360aeb0e81328f783ed4c600d8bda9f94969381a94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:17 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:26:17 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 15 Apr 2026 21:26:17 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e573c5729f2703eb957362b84f2d609455fc7e76abcd02d105377636d91055`  
		Last Modified: Wed, 15 Apr 2026 21:26:35 GMT  
		Size: 87.6 MB (87597511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ce47dfc5170fc13cdb5b9e8198efbd63c26b348639ec8a33bac2db4bf5dab069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7497530df8948c3856910af9e95dfa87949b794cf3c0a4e1f3348fab41cbe1e`

```dockerfile
```

-	Layers:
	-	`sha256:05ed03f2303b22eb8a3c44c9535b4a583038069e6f117ac2899890bc044767a8`  
		Last Modified: Wed, 15 Apr 2026 21:26:33 GMT  
		Size: 5.6 MB (5631856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf03813b944f2f17bcb6fb3adc348c3d4736968c8fa7d81f1e58152da0a0b3a`  
		Last Modified: Wed, 15 Apr 2026 21:26:32 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:48a0f6e97d2618918dead08dfd84e2b6de3693b60c50b78bb1eed8cc44303d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144638419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfda584cc62f170f72d21938f02beeccd3762132c1c155bb5d8a2f16bb1fe61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:04 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:39:04 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 15 Apr 2026 21:39:04 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c3c3d7a81c8f46931c79b064ae2f6b73ad95b8bf46a0c10f9ea924bd55da2a`  
		Last Modified: Wed, 15 Apr 2026 21:39:22 GMT  
		Size: 79.8 MB (79835444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c26ef98ee258de4be9edb5220aadbe4bedd1fc894840d741764594a6a35fce46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7d52acdd17cb1daa7dc58ebcc7799e590fd6a5e7f7ef9b83a5b9d503fdd61a`

```dockerfile
```

-	Layers:
	-	`sha256:156b03cd88d3f612caa9d4b886948d392fad64cce9f4092044166eef83afb539`  
		Last Modified: Wed, 15 Apr 2026 21:39:20 GMT  
		Size: 5.4 MB (5448132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53478ff8c4b6eb89496cacf1b03bd661f0932cc8c9b6986ec9145909a2cdef3a`  
		Last Modified: Wed, 15 Apr 2026 21:39:20 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json
