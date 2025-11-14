## `sapmachine:21-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:9c783bc04bcab2df93fe16aa2f087707aed14e5954c554610cf1f2fffa689c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:ef9648a6c11e103ce40c6ef4f6edb1ab057dd2766087cf2ca33a91ca6fbe82e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89947424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5938db11102244cfdccf88232156c0fa73856ec446ea72cb5a83d1d186ff869f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791ab6c3542522699b18b4b2fda10a41de03e82879e0cd03d97252391672c1b4`  
		Last Modified: Thu, 13 Nov 2025 23:38:42 GMT  
		Size: 60.2 MB (60222736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a2776bff8e6995e798ce08372414495288092b136213e02967730de609bb67b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf08dbb8bc45cfbb66870458be70153354d1d39de37d6dd98cb6faf73c9e293`

```dockerfile
```

-	Layers:
	-	`sha256:6cfcffdc4cf4cebd83d9c9462b9084ac262d047b5e0d877501117411e4988506`  
		Last Modified: Fri, 14 Nov 2025 01:10:16 GMT  
		Size: 2.5 MB (2518632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cdf7b7292f97406024d21d4c7791f78b3e8037927902df25af79bcb61eb15f5`  
		Last Modified: Fri, 14 Nov 2025 01:10:19 GMT  
		Size: 10.0 KB (10036 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:21f0bfcd5704edbd3081094a450c7d1dae46ca2efb847c5652297323a0dc863e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88285870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed4d33515f406f3b91c241ca929fb8d916c2e4ea5a0ceaefc3a962b2be0cb84`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:37:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27664ca10da91e7ebc7aad2de2ee8bae52c470a8337e6f2a1132916bd6f31b17`  
		Last Modified: Thu, 13 Nov 2025 23:38:07 GMT  
		Size: 59.4 MB (59423913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3a60220abfa4c9244b0df19e382d14534d1a0268596ecd6eea5df7ef7be683cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc719f7a6b880f6885729c7376999cef3f480cf8bbf2bfb483b163f25822a22`

```dockerfile
```

-	Layers:
	-	`sha256:f1df61e2ea71046b244ed9a6930b0437563a064539c9c710c0ad447335ddb3a0`  
		Last Modified: Fri, 14 Nov 2025 01:10:23 GMT  
		Size: 2.5 MB (2519148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5d716b834fabec652076e664194959f9c1280249a8006c798cea160ea3050f5`  
		Last Modified: Fri, 14 Nov 2025 01:10:24 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bae3182777b14eec4d2680555aab2330f85dda2d9c7a26755aefa3085bd4b67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95759103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86e5a097a7b185bf877a0d177c88def7bda31a46fb5bff7ecea81d692a96389`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0953d9a3f9eb601577f0b53de229cb4d25c49707f3a0e3c6fd9e808756034e8d`  
		Last Modified: Wed, 22 Oct 2025 11:50:54 GMT  
		Size: 61.5 MB (61455578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fb0d29bfb5c47a99513943b81fc1de983311c85fba142d42f9a3ae88cb8c33ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75aab15f8dbad385e83e33908ba721f497a3c1e6186d702d5906fe33d80175f3`

```dockerfile
```

-	Layers:
	-	`sha256:4aeb34fb4095a6e3d0b466079ef8c5f958bbbcdb54f642669672baac03c003d7`  
		Last Modified: Wed, 22 Oct 2025 15:08:00 GMT  
		Size: 2.5 MB (2516713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbf855f662e3ab86c9795a46966429b23b8cceb671ea4fad068040d1d9986f0c`  
		Last Modified: Wed, 22 Oct 2025 15:08:01 GMT  
		Size: 10.1 KB (10148 bytes)  
		MIME: application/vnd.in-toto+json
