## `amazoncorretto:8u442-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:061e1866925d30ea40cf99164484f39983dfc847e555b9bd5dbf6c4092d6c366
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0bb5cf54c49a560c78934e7a4cec0c3d2d322feed64ecf967db9e10ae776ebe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103351426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae894eae30a6515e007ac2984c3db16c19d12e3e8e46b8f68ca7a4e1d75ea4e`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474348bcf16d0ae474b5c2ff6a97d4a096364717c5d87a0903a1269455fa7993`  
		Last Modified: Thu, 23 Jan 2025 18:31:55 GMT  
		Size: 100.0 MB (100009565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:58f78a8e88dc62121d4596cc8a44c1fa776b10c98354fcfb64aa1e3b5afb0d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dcd6962c1f8cb006fe0aeddff46569310634d869ade89deea4e8d091ef717c`

```dockerfile
```

-	Layers:
	-	`sha256:c80c2cbb9d1b4f472abe6fb2611c5b9bfd1204906caf278aefffc158f48551d4`  
		Last Modified: Thu, 23 Jan 2025 18:31:52 GMT  
		Size: 245.1 KB (245105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cfd4d2a3ce57e452ca99f24df233249da398ad979ca2f57cb4bf5f646fdad85`  
		Last Modified: Thu, 23 Jan 2025 18:31:52 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
