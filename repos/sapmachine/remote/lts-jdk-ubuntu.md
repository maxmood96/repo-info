## `sapmachine:lts-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:52e0fbfb2cb9f9eadfcba00562113677a5df4a1acfcadc4ca4b5225ab5cefe29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:9bdeb0c04017be20fab7486d9b9e1e79cf9463d57a46bf66d467546c026d9127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244836853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148334f0facc5adbfada800de9c81912cce5704fed267eaadd68c9448ff971b1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e31a1d53948721fb6f905b2ed69ef4d7b64cf496405c10145f192e91c4752f`  
		Last Modified: Wed, 02 Jul 2025 05:13:01 GMT  
		Size: 215.1 MB (215118487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a42b5fe3b2fe8c22a49782c34dfb34e4b785849276ad31eee78a904bcc2dcaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394ac16dfeaf84feccffc1ef3ab7ed669472b6b762f01ab3fcad56bb6af001fe`

```dockerfile
```

-	Layers:
	-	`sha256:a0930c31106480ce646dd4ade8a5f606aeee279d0a3ff91bba2bdc88b2e6922d`  
		Last Modified: Wed, 02 Jul 2025 06:07:16 GMT  
		Size: 2.6 MB (2605377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62192a6cc0bc7953390ede2b65ed3b4b077d312d31679ffc97a78ffc1b6e554`  
		Last Modified: Wed, 02 Jul 2025 06:07:17 GMT  
		Size: 13.3 KB (13317 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:86bc90360fc643b0a0dd51df9545386e215505b1a4214524a371500af8fa80cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242238836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc92ba98e87a89ea57c3a2c6631fb0f48abce2f19c55e152bacd31371c0f4c64`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3615e74a277bf6ee87e30e40c7bcb0e2b9666d34c5c69d32de53ee13bbce7036`  
		Last Modified: Tue, 03 Jun 2025 19:36:20 GMT  
		Size: 213.4 MB (213386937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5561db3a97ef02c0963a7d758e6811137e9ca5d8accaad044b7d8202c7f27a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aac5e5e912cb4719f4d17562bf168ea81c1a4b4160b255781072ac2331d6046`

```dockerfile
```

-	Layers:
	-	`sha256:786e44422814afec73962ac08fcbaacfe692c957c17a3c6556e65b099c154b4d`  
		Last Modified: Tue, 24 Jun 2025 16:50:39 GMT  
		Size: 2.5 MB (2499055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fab5bf932fdf1fe4ae5c54cee562acfc9f49a3bca3ef0f967529daa20453474d`  
		Last Modified: Tue, 24 Jun 2025 16:50:38 GMT  
		Size: 13.6 KB (13591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:97ea6137da772da43c4abe895d2429d3a0d698743076d03c2ede6c1348220ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.8 MB (250838242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a640052f8f921a629110049352d34855c19a99a39e3a52965190ef4e0322b14b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:fca9cbe6eff6a6982a26900c08b4e2c5a46057e9e5386288e826ac4f2cb17b32 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:384c99c6e2b4660fd65fc9823f13a263fb87d4aec3b8f2bd813a7a255bcf46f3`  
		Last Modified: Fri, 20 Jun 2025 09:40:24 GMT  
		Size: 34.3 MB (34321506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6458d4f65c8c62378e25e9454aa835649a60a0d9df5a9160436410573a3d84`  
		Last Modified: Wed, 02 Jul 2025 04:47:27 GMT  
		Size: 216.5 MB (216516736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:333cf733d46a748156d6d1ca2fb4a3cd5f92164cf3ad14ebabdf8e2cf92031e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c42dcd1d0738874dd5cea8e66300197786c59a620a0f7dfeedf8a4f69814f`

```dockerfile
```

-	Layers:
	-	`sha256:1f3f3e75ffc3ef3132c93773eb6ba5a28f5071ba67b32053980920f653af7370`  
		Last Modified: Wed, 02 Jul 2025 06:07:25 GMT  
		Size: 2.6 MB (2607588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209f76f75d4acc088902b1df51527fd0c676b23c418fb6982c85eb2f166b95dd`  
		Last Modified: Wed, 02 Jul 2025 06:07:26 GMT  
		Size: 13.4 KB (13447 bytes)  
		MIME: application/vnd.in-toto+json
