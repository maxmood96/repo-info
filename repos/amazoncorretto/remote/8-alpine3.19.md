## `amazoncorretto:8-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:d68c86936652f72efc051e6dee7735e777293eb5b62dfc1f9ecfa5c398bbef83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5e17d115061d7d5f5206a3338d356ab6b8475922af9fa951ff70c1c7347fd6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103617481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4100d92022c968ba3d20d04978b06f3ecbaa592049ae6a60151b7e0ef5908a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4dcc628e7045df83865102b5a21f89001c7724fd2a4e8ac68451492e90c86e`  
		Last Modified: Wed, 08 Jan 2025 18:09:26 GMT  
		Size: 100.2 MB (100197239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:44ede2b48a6faaf7d330db646a2ee8619319630abba8ad70179732d5a458a149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 KB (255030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f479d95354b42ad49249a28e227f0a4f94d90ef58283269d833fd5a72875860`

```dockerfile
```

-	Layers:
	-	`sha256:fc434b0b2320f2ac96a6426b0808b9842fe5871736f3c41251b473889b21a090`  
		Last Modified: Wed, 08 Jan 2025 18:09:25 GMT  
		Size: 245.6 KB (245632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d5d87ec5da97ab7572c50e316ee98df96020f4cccf19885336ccd35913c54c`  
		Last Modified: Wed, 08 Jan 2025 18:09:24 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1ec3e72344b2e5f49e60316c35a0f75a3bd8a1fd93910db31c4280bc1fc4e4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103369947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48583c3e4cefbf00f1cbedac44571a904db23c37bd82397a3abaae8952c9b42f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
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
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5036e9fa9d647ce6308c7abda7a9239f2d40731bb67f3b5566ddf0cd462416`  
		Last Modified: Thu, 23 Jan 2025 18:32:49 GMT  
		Size: 100.0 MB (100009415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:726d52dee9357aaada71eca6401813c6078e60ee77c0312d2317c20cb11dd576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863dd4a4fedd785ae397decd704d4a12a4e5a81f4de70dc3e8f91f59d74ca5a2`

```dockerfile
```

-	Layers:
	-	`sha256:40629ed2360707c5e15b750610bf7a59ebab53fb3ca515c7f54250552cbf2d26`  
		Last Modified: Thu, 23 Jan 2025 18:32:47 GMT  
		Size: 245.8 KB (245764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2ba8b01d9f211f2de99eb0ea0cb6197dd2a90e6976e0c0195d2d05e76a0e3d0`  
		Last Modified: Thu, 23 Jan 2025 18:32:47 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
