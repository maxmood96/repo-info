## `amazoncorretto:17-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:c9fe7e3a08ff2b132095c98d85097f1ef2167f532710a0b7a33d885c99b3819e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8350faeed47bff297e8692f5a1bf35a427271bbe7ea30090c00cc2f41b83790c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149172769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596d82b758866d7447db84d9839d0d212e61253d8f5f7f0c99c70a6d0cac5a11`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc87d35b9d2bc0647974123b8907d47c13122c573a97b743802ee8e0e6690ae0`  
		Last Modified: Thu, 08 May 2025 17:09:05 GMT  
		Size: 145.8 MB (145751901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d9a3b80a12874ad04eae3287c7f7e1eed7f06446939f6e871e5dd410eb012f30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 KB (390310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ee2f4cc02de75948fc86baf5499ecd27fbe55a76101aea6274a0da2d8fd8b9`

```dockerfile
```

-	Layers:
	-	`sha256:f4addf899e6080da6a19ecce53cab5b33b52084f21549c5471e51ef5709ab5cd`  
		Last Modified: Tue, 15 Apr 2025 23:55:38 GMT  
		Size: 380.9 KB (380893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa02a5e64e48ba55846de3af4f9251fa80f8271590615180781c6a8f0fa4380`  
		Last Modified: Tue, 15 Apr 2025 23:55:37 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f9da902b71b51caeeac441973ec1537f6d68d8af42a33d52c827408ef63610bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147457191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f8a6e03842cc5b83d141fde2f715043fa5c1efcd03ef55b8c2e0a394b09d2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 14:31:17 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2b5b348ee64072cad23f06afd5e03e8281f469fe159f778e39fe827ce9e8e6`  
		Last Modified: Wed, 16 Apr 2025 00:14:05 GMT  
		Size: 144.1 MB (144095767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5ed5b622b607b183e01700749f350f452320207437d260881af8b565e2755c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c162775a704708df1388ae4cc6da96352ba9ca2f5cc388b5d6dd88fdf8dbb1c`

```dockerfile
```

-	Layers:
	-	`sha256:08d3b96ef0a1185b1e92dd2f33beda0b2781b9f5ecabaaa6d2522e8f08b0bb22`  
		Last Modified: Wed, 16 Apr 2025 00:14:02 GMT  
		Size: 380.3 KB (380312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038cc0628b91eb0950ba1041bc6708898ac368490912d4a04b791d970d47c4f3`  
		Last Modified: Wed, 16 Apr 2025 00:14:01 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
