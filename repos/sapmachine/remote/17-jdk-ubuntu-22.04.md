## `sapmachine:17-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:0704450d18a8fb1381d1bf88ff2463ba1d7eba9c5fddf0db1f7d8a58a3a612b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b1570e3fecbe9d8363d58296e851436f31c81a3f1c40933b56bbc52764b5eb61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229635535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a3bb373991da3e152d3f18c9ea0f2718d7876559ee59aded9a0c823da357ab`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab668110548a85f839e2d26332ae85f4016e238a39c719b74a79a4d83074d64`  
		Last Modified: Tue, 12 Aug 2025 18:11:30 GMT  
		Size: 200.1 MB (200098542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08b2b0786e8882c733fafb047a13ede9560e0bfb285ca84166805380fa27ae45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433596cfc199f89b16ec2b78b80a2e4ac409bd8d8527f3ed98120751a1a3f046`

```dockerfile
```

-	Layers:
	-	`sha256:5c5bf6a73fec5024b3d3fb786021f878c3f4a57c2020bc6faf7f5a50eca9443d`  
		Last Modified: Tue, 12 Aug 2025 18:04:54 GMT  
		Size: 2.6 MB (2627847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a1f5f9456a4dfdf26be46dc6d6288787bec0c8fa20b27a704ecf34f32d2410`  
		Last Modified: Tue, 12 Aug 2025 18:04:55 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:45d7076ed59fd6151c1cea4580fd59dab0102bd847b9c9a29233ef3788212183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226131267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c76a5cfc0e05ad1ac1bc4c5d184e6632534be2ad3e3cf50d1f1613be565d78`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8062adf3253b3f06eceacbc812d0d63594ba9dfa5f60c08d2b6910e2d9a41ba6`  
		Last Modified: Sat, 16 Aug 2025 00:45:49 GMT  
		Size: 198.8 MB (198772020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:278250a776bcde2b2af75b6528aeefcf4063cb166df3625fe3cd9e1a79a79ad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebdd6a51f4bf522ce5ff634437f998c0e55a23af17783c6ce3ecac6b88d8a49`

```dockerfile
```

-	Layers:
	-	`sha256:2b36e7047975d4dca10ef05c5f8526bea354d3888fd07c5c8e5efd09aa2f0767`  
		Last Modified: Wed, 13 Aug 2025 00:05:09 GMT  
		Size: 2.6 MB (2627577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01a4015731e051889b3a244a34440dc7ebafe438414e969c9bd2ff5bad231d3d`  
		Last Modified: Wed, 13 Aug 2025 00:05:10 GMT  
		Size: 10.3 KB (10290 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:aa3991df089795fe431cc47ca399b85b25fd4f85788d00caa471e2c66f5d39e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235210349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffe9228d50477642f0031914ce48e39a26ddf08ee3037baa1dc8c5f9910bc59`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817647ae7434b7f0f28abd3ba3c05f8744ca1ae0a0d48f0fa5d59d94e0c6763b`  
		Last Modified: Sat, 16 Aug 2025 00:46:11 GMT  
		Size: 200.8 MB (200767204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5d69245902b4c786aaa5446a88032e8830a2953d7416d4f80f6ed956c5c2ab78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:584f8865f37d855bf0b394b8aea05bbd7be5d081a049a6bf713181c30126770d`

```dockerfile
```

-	Layers:
	-	`sha256:deb717b65e8004dcc0f778aa399f8cc60684028574c91d43594a32a059881d4f`  
		Last Modified: Wed, 13 Aug 2025 00:05:16 GMT  
		Size: 2.6 MB (2624040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b65116b94fbfa1673a9aa1add267b366af3a06511e605bc1a836c9ed7484215c`  
		Last Modified: Wed, 13 Aug 2025 00:05:16 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.in-toto+json
