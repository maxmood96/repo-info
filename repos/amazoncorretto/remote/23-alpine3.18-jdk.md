## `amazoncorretto:23-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:ee2ae3cb682ebc98db23279020ebb660ccbaca41a29984a11a701c5a1cbd3d19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6a4b95efadb78f4f8147981be54af7d4208c584ccc20347630b0aea6cee78a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170076541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e2854087c78edc067d53740401feb7f130a94aceaa2b43ba37c975f9dde0c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2422ed9175222718605f3aefdd9ce6490003e6786ccbf4d5e38befddedf56c`  
		Last Modified: Wed, 08 Jan 2025 18:13:42 GMT  
		Size: 166.7 MB (166658567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d88b4a1f883fb8e5c464736b99f73c48d2c0b3c5fddb5d0cbb1708dc46a44710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 KB (391491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d72a066588ae458784488716c166a9706fd45f42b2829b685088c5f231dd5a4`

```dockerfile
```

-	Layers:
	-	`sha256:f51702e161ad31500add866a0f8f3d7db05397341e17a836d373678971c9e443`  
		Last Modified: Wed, 08 Jan 2025 18:13:40 GMT  
		Size: 382.1 KB (382078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12873c77dd9138b6e6c38831a1490cf550a23b8e50ba9f867a49d0035070b291`  
		Last Modified: Wed, 08 Jan 2025 18:13:40 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:486984a29c9bf12584c0a89829046b9a35544831f914dc97b2cce2f5ac8c3f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167690571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119ebfebace29aa293372fae334edad07bc1804791bd4fc87125939a512cd1c6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28af2a6e39f5468c4b86a767a576f9a01b349842f2d90dfb87c305653d056011`  
		Last Modified: Tue, 07 Jan 2025 07:25:50 GMT  
		Size: 164.4 MB (164353136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:719b7352f9529ac72919156290d4943917630d1862b503f4b195eaa70ceb212d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f5f8b36dda15d0071814257b6940ab68025f63fd446d7cd440778105c2aa76`

```dockerfile
```

-	Layers:
	-	`sha256:025755d320b841fb3198d51f1829afec0ff4dedb670e0d9a3412c1bdb3ffe164`  
		Last Modified: Tue, 07 Jan 2025 07:25:46 GMT  
		Size: 380.9 KB (380857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:357230a2c89e7d45e22a86227c284a54ff2a217a43a62076b936d93f0db7074a`  
		Last Modified: Tue, 07 Jan 2025 07:25:46 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
