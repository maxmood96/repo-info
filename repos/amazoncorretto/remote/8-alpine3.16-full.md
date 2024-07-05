## `amazoncorretto:8-alpine3.16-full`

```console
$ docker pull amazoncorretto@sha256:92711924647d1ea1fda278eb20e2ccdae4ff2bb1105e666fafa685861bf83889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.16-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:91b1ac09f25dbe20e1c9a79678edf263371b5fce769daab087596730e71ab976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102979351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2a50511371809717ec413c047913c76dfdf8606f2bc94677d347275f93fb6a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e8d3e6f76514ed73fecdc57a70e346b410ad0bbb9cde1621858920aeed2d67`  
		Last Modified: Fri, 05 Jul 2024 19:56:02 GMT  
		Size: 100.2 MB (100171514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.16-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5a660cfca57dc50656a99c9183cc286a2799881f83fe9a43ef2361c9446c95cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.2 KB (245163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0bddeb0424842792da8fe32a15b68804929be3c50383a957597f0dfb6998c6`

```dockerfile
```

-	Layers:
	-	`sha256:b0ec263dd514d881435d6c5234034ab2e2842e518c88829af39d024854e9c8b6`  
		Last Modified: Fri, 05 Jul 2024 19:56:01 GMT  
		Size: 236.0 KB (236010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2670f5fd2c53de4a33cc6b7d4dd53071c9b828f50aeed92e8b3f4a3cabb5feca`  
		Last Modified: Fri, 05 Jul 2024 19:56:01 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.16-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:06f35690d94e55a0971f41b2f0b90bdb4b72e32ee4119a47ac5d25991487397a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102527111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f229090aa208ac0ff89edfc002d08459565fafcb439011f0e284f5db55ecfc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a6e568580edcb1d68bc087086cfd5220b39e0465d61049841bbdea479ba8cd`  
		Last Modified: Fri, 05 Jul 2024 19:59:19 GMT  
		Size: 99.8 MB (99818828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.16-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:59dfe64095120a569b965b9f54fee58074db553040b64d633e5baaefd5918b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 KB (245593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2402e53d82624aa47357dd58658aaab21fad79907a0679e3c3f37962e81cbe47`

```dockerfile
```

-	Layers:
	-	`sha256:59fbdeb91a3e532a5e889c33353bbb9beffbf7167249a7eb1fac7940cb91549c`  
		Last Modified: Fri, 05 Jul 2024 19:59:16 GMT  
		Size: 236.1 KB (236142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08a8d7ee034e5f8edd9d4a386ce7b073f84123f346b548de5dbd948d0d61633e`  
		Last Modified: Fri, 05 Jul 2024 19:59:16 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.in-toto+json
