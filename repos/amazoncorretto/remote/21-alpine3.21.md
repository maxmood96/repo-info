## `amazoncorretto:21-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:809decf63e8065adb13ecbee61f0955c1701efac52cc76b1451e66e97fe4cba4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d0dc9f402d7fd5c93110b32bed008077335ff3a307f43e4db6954da1ab6e35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163026626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560c195e0b1cec61e30cba6e815df8d7bd0c5c1f7a15f2973fdc5eb0c0dfac12`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfc4b2b21c9c6dbc83ce5192a19ae174ced20e1048d0f4879281ee4810557a2`  
		Last Modified: Thu, 09 Oct 2025 01:03:22 GMT  
		Size: 159.4 MB (159384057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0e2b0e5856b4ff525a44c3965bfc18a62e97aba08a506f7a5d3da852476cdd04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.3 KB (393293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799b411486119dcddf98be66dcf74508dad618de5f00be8a27f7053c19673dee`

```dockerfile
```

-	Layers:
	-	`sha256:c787a29d051b0b6f53402ccebcf5bc1ffcf7369f80970fa069f50fd615a44248`  
		Last Modified: Thu, 09 Oct 2025 00:50:12 GMT  
		Size: 383.9 KB (383879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24ce82220a8a98130bca52aa833b89b006fabbfa663b38e2fb140d68a97a49c4`  
		Last Modified: Thu, 09 Oct 2025 00:50:13 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8c7a36b861c37330ae0d024aa9680ea8ae0d93daa1ae2597d7deee9546986e98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.3 MB (161334086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9b8b86ee363f49ae7434a13ea72f0f2a972968d39bac07a0c3af858ded8f57`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c54a9e29e1473dfb604e876d45a00b91c8582290215a6dac4effe99d54a6909`  
		Last Modified: Thu, 09 Oct 2025 01:07:16 GMT  
		Size: 157.3 MB (157341733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ef152b67fa67577bd024c94e09990b44302ae123a2db5afd024b8e54cfdf02fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.8 KB (392816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b977384b997cde6f54247ca0225834f3304aad5836e45d6e1a2ebc7ab37c05aa`

```dockerfile
```

-	Layers:
	-	`sha256:2e68e4f7154066c4ed7384aeeada310ffa36000f4a38052fdcebe818e5b59978`  
		Last Modified: Thu, 09 Oct 2025 00:50:17 GMT  
		Size: 383.3 KB (383298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c1f7c8040704be9774a39cc509cabacbf9dfcea8e90058d8edf84dad151cfe9`  
		Last Modified: Thu, 09 Oct 2025 00:50:18 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
