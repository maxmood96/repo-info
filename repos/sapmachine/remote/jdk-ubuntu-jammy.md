## `sapmachine:jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:fdb6e6026d1fd2d9827d785a37850b04f4bccb5e69fa95454d491690ebe778a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:17e300df56b84998e7fb75addbd5665631ce8273058fe26d62c9b7fbd04c2484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261584676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3cf6bb74d28031e3797ceba661cafe6706e53cb1050e6673eb11b4dd56156ff`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa83eebd6eb9994c3d94fc86da6b13d223b0aa226b8681d2c9b5edec9a09308`  
		Last Modified: Wed, 02 Jul 2025 21:04:55 GMT  
		Size: 232.0 MB (232048990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ac34afc9f751633ca2094cb4eb817c9b07cd26097cf2befbdb3aad8b4d8e391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fee88a9d8591bf895e3d96121e57e29423005d7e5ce27919bd5e069915a34f1`

```dockerfile
```

-	Layers:
	-	`sha256:c69d6f4538c678ca6514f9998cec2d7aa23870e7a9eb0255500e5c8dc466acff`  
		Last Modified: Wed, 02 Jul 2025 06:09:34 GMT  
		Size: 2.6 MB (2621720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40278c52be45e0591fb0d622ca2e1e39edb70530403ede26f01ac7e0db4252d7`  
		Last Modified: Wed, 02 Jul 2025 06:09:35 GMT  
		Size: 11.4 KB (11413 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d5961900fc244d477f5c5b75a6806c29a48a2760940cc1d1956011283d67dc94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257273278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b241b3271dc7e944a757e9c96e38a4636ce2b035b0a91d9a17a66853077a3df5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef891b7929d17494198ae65ea0bd3e600df331759f640c2e5ac921702a0af30`  
		Last Modified: Wed, 02 Jul 2025 13:40:33 GMT  
		Size: 229.9 MB (229914006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b73b12a79550946b335d15e73158f41c1fc338eff89c781ae9b2fd5eda5efdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b564990374ec020fc19137246a23aeff007e2b2118cc078369e5f10b45ccf359`

```dockerfile
```

-	Layers:
	-	`sha256:1aa71051f4933eb3934a9b709a63dc3216c4624605f705ed0df9fe535f1fba78`  
		Last Modified: Wed, 02 Jul 2025 09:08:20 GMT  
		Size: 2.6 MB (2621495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68199dcb0a6ff79ebd2fb9ab319591d9b2777e08e4591aa18740f2619d646e6f`  
		Last Modified: Wed, 02 Jul 2025 09:08:21 GMT  
		Size: 11.6 KB (11613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ca8a332df1858f5cbf64c8dc628e57e15155310be53d576c08030a6d9c140ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267694443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1aa955a1f00b77025198d25770dbb02123fc7ac4e77cdab12c64878a6b435e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6870bda15e2649a6330cc0cb4b8ea22e8c5c2f5e5e9bd6b341f6ec412e988e6a`  
		Last Modified: Wed, 02 Jul 2025 04:41:45 GMT  
		Size: 233.3 MB (233251822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea6ef5574714d711aec09d9ca143f1b809f4f0db63f5d5592568dc00c875cda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a07e1516f1af048c5eefb382e58671d31e47b8e53976716ebc7cc3b157f7f86`

```dockerfile
```

-	Layers:
	-	`sha256:8390c91e1632821e1c70c2455aa41d9c6b3978d5d84db9f7d91c887efeaa4a21`  
		Last Modified: Wed, 02 Jul 2025 06:09:44 GMT  
		Size: 2.6 MB (2623335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7055e7d0f47091b032a544300014eb75118218ced981da64d5d4a9472f04526`  
		Last Modified: Wed, 02 Jul 2025 06:09:44 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.in-toto+json
