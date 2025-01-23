## `amazoncorretto:8u442-alpine`

```console
$ docker pull amazoncorretto@sha256:cdce1dde0fb4b1581d3535077b08af20a3e3366bdd9b60afd085a37c53795eed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-alpine` - linux; arm64 variant v8

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

### `amazoncorretto:8u442-alpine` - unknown; unknown

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
