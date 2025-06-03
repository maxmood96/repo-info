## `sapmachine:17-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:9394a4623ff1e55b260c7b1b7c14dfff0489b5afd854df08dd292084b184e718
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu` - linux; amd64

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
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88e1fd427e67cdcb1e6802f0795c7102e2b809be1f751e670808312869915e5`  
		Last Modified: Tue, 03 Jun 2025 04:17:51 GMT  
		Size: 54.2 MB (54212906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

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

### `sapmachine:17-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:67336e7f0609329d26f30b362385e54e7a26e488b130f0114548dcde81dc3c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82511880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816b669a7d38e885be32d884eccf699239f43e43ffe9244f4135b5c2289bbfad`
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
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Mon, 28 Apr 2025 10:53:55 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7804db7a28da6f222f5e269e7bf813df3e1a165f31eef569a41002c3c12af37`  
		Last Modified: Mon, 05 May 2025 18:39:50 GMT  
		Size: 53.7 MB (53665004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:43796726751ce548a010ec3b11d6afbbce6ae7a8102eeda05e98852ac4dc8f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f792a2cbd9cabadc93a5f106645421786d021263e5951c760ac6a4cad9899e4`

```dockerfile
```

-	Layers:
	-	`sha256:5fa298b4826aeccbae525df72d65ee31b080f0feb41ec195e4f6cf90c0c2e5a8`  
		Last Modified: Mon, 05 May 2025 18:39:49 GMT  
		Size: 2.4 MB (2386076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe0922e04755cc8aec49aaa8689a80de0b9fbf36412e04e543ce31c09393fb9`  
		Last Modified: Mon, 05 May 2025 18:39:48 GMT  
		Size: 9.6 KB (9599 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9d689bbbc02727ee5bb54078632672bbe6d94c49981239db60fbfe438c8a2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90182746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af958e2bcd8795b7593aa9c0aa6c3f3791575b7906e599f4f21d116c234d2e7`
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
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
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
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Mon, 28 Apr 2025 10:54:08 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf6854222eefe1c5168047ffeb70c61547af59ababbfd6f18a9f0f6fb16f7ab`  
		Last Modified: Mon, 05 May 2025 18:36:37 GMT  
		Size: 55.8 MB (55841908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ebc63836b5899e65d0774a7194df5f50019df103299b32dd7cf72cb9650ec42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef8906c9be4b99d619071d46bea7a4abb6937009e240a8cec5a1846dfa78aa2`

```dockerfile
```

-	Layers:
	-	`sha256:320afcb68c38e5080a991d1c6da52b64c1ec1bcca423f2b99da0006e25ebf137`  
		Last Modified: Mon, 05 May 2025 18:36:35 GMT  
		Size: 2.4 MB (2389535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f84774ea5aa7453c6aa0a30807b12dc5fce63ec08fd207305e23a7cbcbace7`  
		Last Modified: Mon, 05 May 2025 18:36:35 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.in-toto+json
