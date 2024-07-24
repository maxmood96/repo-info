## `amazoncorretto:17-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:b291536177d8dd49c57ac2678fbde8b4cf5f602b599d99e8b1366bcbf989ab57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ab9dd3170ae090b17cebe288f2a707e406b8b4792132db7dab2f30e12976749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149437053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f130ca3cb52e319328246a029cc2541a5792d5d9ed13402d63718478a450cbaf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdad945e55a69e381ba8bc3a0972a33ac83c2c5acc8569b6368eaca7448eb088`  
		Last Modified: Mon, 22 Jul 2024 23:04:48 GMT  
		Size: 146.0 MB (146018013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:08bbba5498b40eef85c3d1801bd3262a247c721da3bf45d0f78cabb93fc95cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.9 KB (389935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b522794bcc3b8eb441338a890047f311384b283371df56ceaa3f4678575cb629`

```dockerfile
```

-	Layers:
	-	`sha256:6e7ba5cf08af4fbb7a15eeff3eb53b7e9d590ec2d2d3033e0f825eda8aaaacb9`  
		Last Modified: Mon, 22 Jul 2024 23:04:46 GMT  
		Size: 380.8 KB (380763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d75ff49673ff2301a4cf9ce4349f358b623f5a14ec9178e1dd5c9d3b033c79c5`  
		Last Modified: Mon, 22 Jul 2024 23:04:46 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f7b00665ae4a64017b2a2b5f0d296f43a7a5a10a339d680672f9ae7c1252fcfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147709240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e87cb7da669ca943023f3d6313f8baf40f7e101065e124db3ee0eb3f9ccb39`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fddf05f12fc371ec4f863dbeaeef32c38189c857b345fc04832f161b61949d82`  
		Last Modified: Wed, 24 Jul 2024 10:43:41 GMT  
		Size: 144.4 MB (144350782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ee470bf1d0f6658eaa63b4ca346a7c82d3ded5cfab58e61efc682fc1a7f62eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90109ada9799d680dc866d31853abdf2adcb751100b02ed6ec80562e2f57ef83`

```dockerfile
```

-	Layers:
	-	`sha256:445ae13f824fe39eb48bd291907e2b550ea35dc33fc3f63b096b82d045087a6c`  
		Last Modified: Wed, 24 Jul 2024 10:43:38 GMT  
		Size: 380.2 KB (380181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1296d2017939cc0506e73a7c4062929eed0e019f9b9980ee9fdde00d32760d6b`  
		Last Modified: Wed, 24 Jul 2024 10:43:37 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
