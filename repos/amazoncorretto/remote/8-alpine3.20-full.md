## `amazoncorretto:8-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:3e736176bc3593a299ae45d830618fd75a9a0812a79a4f96283042e40385d449
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a45f517690c50dbf585682aa61d860aeadb059ffb72d62e3a0f89818cadbdaed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103875246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b49941f21e232c3294c544204ec2763175203135d00e6cac371f5ac24ada49`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504841a2cef45f5881b4af506a0dc4c2199f3e158b1eddbb4d6190c3ac83b7bd`  
		Last Modified: Tue, 15 Apr 2025 23:55:21 GMT  
		Size: 100.2 MB (100248349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e4eeef6e4f894703cd9c2e7112c34875ed1893cc355d384221348aefed88dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 KB (250799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ad4cdb43d2d6f67829021117aea7bec0e7b69c4bfea226238f4ae8676b0e55`

```dockerfile
```

-	Layers:
	-	`sha256:389eacf77f9008a5245d2c409c1f963adc45ce0d2f6d194d0de97425b6f8bb79`  
		Last Modified: Tue, 15 Apr 2025 23:55:19 GMT  
		Size: 241.4 KB (241402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b6c90ab511ce145a2d98a43da8f1cf97ec45e66dff584415d8125b2b57bba1a`  
		Last Modified: Tue, 15 Apr 2025 23:55:19 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:367652ee381275b7f667552e8d5c389dd1b4543e34b37ec3bd854b411d1bb37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104108029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ec3a543ee7f3293a3ce5e8f1b84201eeaae5bbae26e62b7430e0cacebc4e5a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ef00db246e3486fce2b00e747f353d617ac532848531d7544b4bfd43afb2cd`  
		Last Modified: Tue, 15 Apr 2025 23:59:24 GMT  
		Size: 100.0 MB (100016864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:351c85b9e244fc39492725a166b4707e2a7f7466dfc44199e796a43e3fcba97c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 KB (251033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fb55608ed94be85e8d4d9035e4fec40e5340d3aaffaae9922bf1d53b144d4b`

```dockerfile
```

-	Layers:
	-	`sha256:61ae0505a967d8aa16ec323010a9292d8131269a561f61a013b8bcf8dd3099f9`  
		Last Modified: Tue, 15 Apr 2025 23:59:20 GMT  
		Size: 241.5 KB (241534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52fb9973f8d1bed4a77c8687fc6a1eec901b5697ffc7346437e932296fa13c3`  
		Last Modified: Tue, 15 Apr 2025 23:59:20 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.in-toto+json
