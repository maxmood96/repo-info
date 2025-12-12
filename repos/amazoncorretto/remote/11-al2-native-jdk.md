## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:af76c78242e25a8297b5e819d6725f651539fdd6844aec5f70a224ceeeaeff34
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:30b77fed4dbecd19a1c82e77add01e98122d6b61d4842032f10b68c60f9000b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224529240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499bf20858bf16a489aefdf7893412f32e87c4ed8fb5af1d3a29e09c651a63a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:37 GMT
ARG version=11.0.29.7-1
# Thu, 11 Dec 2025 22:12:37 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 11 Dec 2025 22:12:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae059b96e53b50aac9cda44da4d46915d763d1e3215ea5510d2c3f06e473f2`  
		Last Modified: Thu, 11 Dec 2025 22:14:31 GMT  
		Size: 161.6 MB (161588265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b32d2742ea70559f82fcfa9c3c377b3d1bd79185f9b66dc69c3fec7749cf210c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828943dc2f4219e520267c484e8e6ba144a4552e2822cafa7f6f78aa66dcbbe8`

```dockerfile
```

-	Layers:
	-	`sha256:86a6c9eba3087ddf1cd67b5cf4d12321a06ec5207cc86a2e31a72290b2447354`  
		Last Modified: Thu, 11 Dec 2025 22:47:40 GMT  
		Size: 6.0 MB (5995082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c8a35e2e3909ad03ebd33dffbd2d3092e1f75a2fb97d8627ae31b7a09d1863`  
		Last Modified: Thu, 11 Dec 2025 22:47:41 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dafaadf082b7f68dc4d8f8ca8e1c470439e929172059358a8efaded95eb977de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216455090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6124312c4f9257b34466abe4f902e61561ab8cef8fc21696a1e210be11fa409d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:57 GMT
ARG version=11.0.29.7-1
# Thu, 11 Dec 2025 22:11:57 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 11 Dec 2025 22:11:57 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488125d722733825e12051dfd1cca311ff5bee8fc60bab907aa052100abcfc2c`  
		Last Modified: Thu, 11 Dec 2025 22:13:41 GMT  
		Size: 151.7 MB (151659335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e52133fb090a3cdd601e23eb0623ba076071d6e06623c22f9e06b22c8bae2972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7134b7c2af9ee84d41ff96a62c3094c82468b618896921563be280413a9268b`

```dockerfile
```

-	Layers:
	-	`sha256:495f0b1e1379a1ee8b85edad7fc855e2cb1ac6f373679ab08735369061585fb5`  
		Last Modified: Thu, 11 Dec 2025 22:47:47 GMT  
		Size: 5.8 MB (5787796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9599726c0e43cd40538e57b721b4843d0b9dcf8539e517873843ca6676317c`  
		Last Modified: Thu, 11 Dec 2025 22:47:48 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
