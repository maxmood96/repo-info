## `amazoncorretto:8u442-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:00c771903fd6e691b3cb4af6c3e09d50fe5bfbc44fa7ccfcc7c1fa84a618622f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ec82fcf94f240dbf0f4177cb2fd8c49f7d178f22f10fa3cad9d9001aabd0a932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44703954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b347e9f912c43c61eca73d7654474cd34a0de17927b73163f4782aae423b95`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=8.442.06.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80107f328542d43844ab4a5b84f1b0d25d241cb8e57916de80c9446f5443c529`  
		Last Modified: Thu, 23 Jan 2025 18:32:15 GMT  
		Size: 41.4 MB (41362093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fad32e6e281bf70b478aaac903f505d97894f148e2951497c248726f0f758622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ea1dcb0087eba19c30d16b0d8ae59b2d83e8f2608c71ca3ada3e3da2247b13`

```dockerfile
```

-	Layers:
	-	`sha256:1705609fafcb811a140d8d17164bcc5c36ea2d864d2d53a628db8fb4923cf9bc`  
		Last Modified: Thu, 23 Jan 2025 18:32:13 GMT  
		Size: 184.8 KB (184780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee492cbebe94cc4a0d932a0d576e2036401f15d224c4e37b7a4090d63b0352c2`  
		Last Modified: Thu, 23 Jan 2025 18:32:13 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
