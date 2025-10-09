## `amazoncorretto:17-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:86a5bdf7f370ba6167a873c854ee8840a72207d2a0f0adbe096ce246210b360f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:597b3373a433bd5e2359a329efafc568a812af8917f364e6866088bd947c3cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149669390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef706c81b1c5046d3659e6815888201c47b802f677c4554c4ec1bd89fda021e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:e10c890b7504956ba5fb8189c0e82584d15fa49f18879104df6ebfea47eb108b`  
		Last Modified: Thu, 09 Oct 2025 02:09:20 GMT  
		Size: 146.0 MB (146026821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3be338f6d02b979e2402dd25b8f2f20197ef7c421a4f5aaab6afd2764ff1054a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 KB (393399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a2cfbe319b9989f94da6faad1907c5fe7bc55fc7107b6e28ea77a78fe50687`

```dockerfile
```

-	Layers:
	-	`sha256:80ced66c1bfc2d3a86c5275e235d8d78b424f8b3bbbab4cad3e755104a893dbc`  
		Last Modified: Thu, 09 Oct 2025 00:49:04 GMT  
		Size: 384.0 KB (383982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0107949fcba4a69e8178ecf77d029ff72d43e00747a3b4f059f42146544e4582`  
		Last Modified: Thu, 09 Oct 2025 00:49:05 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:98feae02ecc649e22cc8acd9aa471b89e0a6c599b7798643e36e14fe4cad6e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148312844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86bd5ece4d0f4ad4c73a0a7ead33527b7897ccbd9b27e92b25de8927132fdddd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:268046968284007bafc5a64c5e27dd757c91ef432a37f7036b861632bd6ac1cd`  
		Last Modified: Thu, 09 Oct 2025 01:34:02 GMT  
		Size: 144.3 MB (144320491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:546a26a5440a06ceed73f00921e1a1da2494e3e064c408f021b046a7b61a37b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.9 KB (392922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e3ff3007dbe27f8abc8aaadf66c5e5ebf539747f3a34d4c6282d74035d28ae`

```dockerfile
```

-	Layers:
	-	`sha256:be8bd6c1d92892da9c7746c05f9e7763290c134c8fa35531da7db04ea8e214a4`  
		Last Modified: Thu, 09 Oct 2025 00:49:08 GMT  
		Size: 383.4 KB (383401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8115294e2e469e281f22f75068ec72e7f3b6bbdf69f0ff8a16b72214cf89798f`  
		Last Modified: Thu, 09 Oct 2025 00:49:09 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
