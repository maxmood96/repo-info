## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:1f6996763ec1eaedd0cee06529f76c99ec3ddc1fd4cba57d1bbb3d0d04b822eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:104499915feef9440299db478365621099ae6ddd957a5fd320853bc4467a7541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83928243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c4bc79b5fa111c89d7d391edd6c778f3b30404d8274553f16c6d9b98136bee`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88e1fd427e67cdcb1e6802f0795c7102e2b809be1f751e670808312869915e5`  
		Last Modified: Tue, 03 Jun 2025 13:48:34 GMT  
		Size: 54.2 MB (54212906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cb7a6fe6adf8c0c3064ee62532cfe8a971c8b2dfe5e635faa0ec3a2e8aaa5f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb87fb4c0d47bd751c605aeba5a408c5d409a69bc9b200361b2624fe7bfcc2b0`

```dockerfile
```

-	Layers:
	-	`sha256:6a66e783ee6fb17ea53efabae351a569b229540075e29c9988d80db5c943ffe9`  
		Last Modified: Tue, 03 Jun 2025 04:17:50 GMT  
		Size: 2.4 MB (2409792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c59e966f20e5ce76ecf6349d304678093660f9f00295b792f66314894fb2ee`  
		Last Modified: Tue, 03 Jun 2025 04:17:50 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:aa0d5d3a9062e80ae7cd3b26421ff5e9008992681770a746c366d7d677e294bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82517325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021dbf6da4c2bafd3a81207b3281151a31cba9977c8ed0db1314f23de2893a21`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5324c412ba16aea76c61e952fa9e273d676f1af54ae97bfa6c7602888a0f4c8d`  
		Last Modified: Sun, 08 Jun 2025 06:42:37 GMT  
		Size: 53.7 MB (53665426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ad5b11faf6073d24d47c9b705fd77b02824465dd9eec6b098b9599e008d0121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cde9e3b67bc56ebf8cd171542769a446f4eb03b3d366dfd4bf5bea665479010`

```dockerfile
```

-	Layers:
	-	`sha256:fae5e7f852b06f89c5b7cdb3ebdfc4beabc12f7c59d172b1a10807da3930fea2`  
		Last Modified: Tue, 03 Jun 2025 06:10:38 GMT  
		Size: 2.4 MB (2410284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a68b7eb95e946b092104ca0669c55854d4b11c5878836654d064de255d60d55`  
		Last Modified: Tue, 03 Jun 2025 06:10:37 GMT  
		Size: 9.6 KB (9599 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b6059cd6b12eeec185921921368883db87a89c70e979d86bd9bf7ba467367f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90167755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c463f6dc34c626488c4a59130e1d42d587b65c9a8aec7ed41c98c3f81739f8a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d017abc18760ed11d2878fd8c2aab470a2a0d445c0b2c8e54134ce1cc03079`  
		Last Modified: Tue, 03 Jun 2025 06:19:19 GMT  
		Size: 55.8 MB (55842545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6fd8e1885a6d9b053ae59235c07de14c67ecf6d51d272bf273a2fc5021182ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2423403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5c53bc02ec30c9b74cfb76d05e1c64d8453fa519a4353e55b3c67d06720f25`

```dockerfile
```

-	Layers:
	-	`sha256:dfac4823e6bdc329537c68f612c0a99f49f22d6025407ab4d657c4c6d67caf66`  
		Last Modified: Tue, 03 Jun 2025 06:19:17 GMT  
		Size: 2.4 MB (2413877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d7d7f338290bd82eb621f46ba0e240ef24048222f8c7ea45391db5d76afa75c`  
		Last Modified: Tue, 03 Jun 2025 06:19:16 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json
