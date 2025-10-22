## `amazoncorretto:21-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:2622b23e1a0287ab6e2a0abb0faab15f4070716dd5e6a70bebf1b1dfd48bd22a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:016b5a4d74cf71240f71ef5358afdc5cd793379b6a1aa8da7a094dda140d120e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165379996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5aa1730df25f8a1ae24c14c11066b17d19f3fd52a4aaca3092ce55b2573254a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0232a5c1ec36753528564a0c37c51dd325df2a291ba8a36a4d16515714648b`  
		Last Modified: Wed, 22 Oct 2025 00:52:18 GMT  
		Size: 161.6 MB (161577544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:475e7b16e152611b573a6c1e6ac9fd93938dce28ec94872a108b3f715b162a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.1 KB (595062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8075a3fabfa04564aff54aa4fb9286f2bbe40a9112d377e23b49ea7307cf1d7`

```dockerfile
```

-	Layers:
	-	`sha256:be86a69660d55666e135ce93442b5b1cbbf96afa756414c5352b306903e94aa9`  
		Last Modified: Wed, 22 Oct 2025 00:52:05 GMT  
		Size: 584.3 KB (584341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3f17e056d43c90e3ffebccb3c93980d0ca9987d29e99018816c91ad791bfa7c`  
		Last Modified: Wed, 22 Oct 2025 00:52:06 GMT  
		Size: 10.7 KB (10721 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:053d3bd6d3aad67bea261eeaafedd3779624fbd17520e207a7b41d08e7af6c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163733186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fdbe630a2a673efae57be1b5eca1d6144be7567af6e75de9734598b91ca2f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd998d4c35c3887cf9b7d0f274f70b8cae4a0a1bcf69e39670164930f639106`  
		Last Modified: Tue, 21 Oct 2025 22:13:22 GMT  
		Size: 159.6 MB (159595117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8cf32ca326b9656a44b633cdeeae19990323dfbc223a75d4ed6d6a5dd6e8f670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.7 KB (594680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a73944c1698ac762a17a281f3b25a5fbf3a7920bd3a0fb1fc0ff8efa09aa1b`

```dockerfile
```

-	Layers:
	-	`sha256:4b5ddc7a3d0cface24e80cfba26d54ffbb6d7c3edc48d8c9ced397f4d3103317`  
		Last Modified: Tue, 21 Oct 2025 23:15:41 GMT  
		Size: 583.8 KB (583808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dac6e3ce30308f6d10f4ca4dbb088be9a109c35efb92095efb6e814fca689289`  
		Last Modified: Tue, 21 Oct 2025 23:15:41 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
