## `amazoncorretto:8-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:67e3d75abfb1160a472795d1757c862a541c390f3264699a98c493455b396192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e57fb787af51e9c1bb2f3eba07672d58bd4df98efaf6343dceead3d64999bbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103821398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e6c32e6272d4a8111438beb1359f365c0d973838e7befeb6bb7e1058bc430`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a15a91bb85d85949856ba1d3ccade006b10de18ccdc8675614554939053055`  
		Last Modified: Wed, 08 Jan 2025 18:09:49 GMT  
		Size: 100.2 MB (100195138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2c3c5bcc5dc0b0902525f46744dafd0514c313857699fd1f4a186a35a8e0c499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 KB (253396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb0a4fa8b6b6d54bdf84d0fc17b071453750044dc0d4e32e49c03fb537e2051`

```dockerfile
```

-	Layers:
	-	`sha256:f155b48d7d890d1d748e8452ba823b19c45015ad6f536568e904eedca58ce274`  
		Last Modified: Wed, 08 Jan 2025 18:09:48 GMT  
		Size: 242.7 KB (242700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b202bdf0f589e05101c8b41bda428265fa09b14a592c0fe47cf79cbb13d70907`  
		Last Modified: Wed, 08 Jan 2025 18:09:48 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:70ea949d4b76a0d116a56bee4089b90d347f85c3caa485298942b7089ae0f4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104100841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04bfdc720f5889c3a4de21fe5a082cf23837c5525c6154ab941f039d87af98`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=8.442.06.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7095b8d01767496a8a3b5354570296d6bea31e7dd4414ce5cd6f039faa159f`  
		Last Modified: Thu, 23 Jan 2025 18:33:36 GMT  
		Size: 100.0 MB (100010072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f013daf0cc0df91b1cfcf98660c6dc2c50012c37a7205b5289ac6588bed89e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 KB (253728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cfa06d39018ac7862002fbecd3cbeac5569d3d851132647e7848e4aecd6d8e`

```dockerfile
```

-	Layers:
	-	`sha256:89503e1385c1529eda7368d385078882a49a1940750d8a15bff5a2af7ca941c3`  
		Last Modified: Thu, 23 Jan 2025 18:33:33 GMT  
		Size: 242.9 KB (242880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc973c784006350a41e8937f09a1ddbd78be5856f2a1886ed55878d6d9188a3f`  
		Last Modified: Thu, 23 Jan 2025 18:33:33 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.in-toto+json
