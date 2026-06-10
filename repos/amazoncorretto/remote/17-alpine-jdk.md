## `amazoncorretto:17-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:f7e880816f3fa3fea751b8d253f6d2db7ec1e5a957934801995f07201d8d46ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:43ec99d337a7f803181f079e06895bda1364cfc5800e061799e77460dc0360c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152473651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb5afd9285f02b96dafaeb7b32069adbde8d2889aede8403424989256b33d58`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:53 GMT
ARG version=17.0.19.10.1
# Wed, 10 Jun 2026 20:15:53 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:53 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569c90a3d6425ebf27ae605c6f85d643cfc2a5abeccd203ca236c44adaed9485`  
		Last Modified: Wed, 10 Jun 2026 20:16:11 GMT  
		Size: 148.6 MB (148606896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4474054e2ef1b3ab9c7f734a42fabd4b194698f27d81c1152b98623327ec5891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.6 KB (594569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2933bfbd1f86d94ac054547a0292a4cb3dfb44adcde3c5d17d821604351f85e4`

```dockerfile
```

-	Layers:
	-	`sha256:d60c9085cde48ef0ca97a3e64c93a19bc78821d42392b62b8a0f7ecec08ffdd1`  
		Last Modified: Wed, 10 Jun 2026 20:16:07 GMT  
		Size: 583.9 KB (583882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae5d833f3c71b10abe236ac61c39d37e9d4214ffdabb7ecbbebcf2cf80c5752`  
		Last Modified: Wed, 10 Jun 2026 20:16:07 GMT  
		Size: 10.7 KB (10687 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:46836e2f6d5ea2b444642c75010fe38e8f1b6df7d9146cb7fdece2df890d2782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151155862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db610486da24247d4d396e55cee1eae22bcdcb72bba160363f60e8be6817e4be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:34 GMT
ARG version=17.0.19.10.1
# Wed, 10 Jun 2026 20:15:34 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:34 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2292cc84ef6bd7f474f47adf298c1d2f809f51ecbab69da7b8984f449d56a90`  
		Last Modified: Wed, 10 Jun 2026 20:15:52 GMT  
		Size: 147.0 MB (146953532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4a4e5271f2a59b9c2e6b64e79faba506ecb870173bd5417a843477f463a8cc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.5 KB (593538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0077f8f7560bc5b99771dd219bdd4b1d9f45a5fec061f36934b5e299e4a235`

```dockerfile
```

-	Layers:
	-	`sha256:5a7767038f8903719e5c3f906a1137c6e59ce111c2cb8e959fcd7c436c8070ec`  
		Last Modified: Wed, 10 Jun 2026 20:15:49 GMT  
		Size: 582.7 KB (582699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b965bb04d3e0e704b75aecf13ac78322a352ac9460d58d2a2d65d781b4b0976`  
		Last Modified: Wed, 10 Jun 2026 20:15:49 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
