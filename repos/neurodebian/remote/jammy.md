## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:dddd5dfbc7fd007f4a3e728570835205318a059509fe698a32190ff096b1777a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:5f26675bcc90c8758ac288c5e42b178ff48a73e9ab4970f919e5ec4938cbd460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33271586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d5a7ae88d753f13e79fa4bb43d53cbf4cfed9fadba34ab474f4099807fe261`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63336557e3a88e2b6816b75ec69356976ec7a6330214bfa441e5d86b8bcd5fab`  
		Last Modified: Sat, 08 Feb 2025 12:21:15 GMT  
		Size: 3.6 MB (3623158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f3b6cde57e753607cb5d03b5f4df97fcabbea0a03734d33c7a056556b608b4`  
		Last Modified: Sat, 08 Feb 2025 12:21:14 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6389250b72dfd734ad1e61588b821ac38d8a3035405ce0dce0746dc8aa07fd94`  
		Last Modified: Tue, 18 Feb 2025 21:04:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128920b07afa9e2ab5a724db970a1017a3839518a53c5829c82e7a6dce0154eb`  
		Last Modified: Sat, 08 Feb 2025 12:21:17 GMT  
		Size: 110.5 KB (110492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c671d1877f1ca886adc735145c09a8b212ebf717dab82aafc170b00ada8f0890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2068979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb200fcf794b88cfdfe58fbf9fe7c5df4dd58d5af47ef863b77847b1ce789695`

```dockerfile
```

-	Layers:
	-	`sha256:495ed7fc83baeda0269343c97821047e2c68647a9c3b5d70f448b4caa68577c6`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 2.1 MB (2055319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa3488be0939d3a148d71befa440ae927009daca74013dc5ec80152a7933da1`  
		Last Modified: Tue, 04 Feb 2025 04:24:58 GMT  
		Size: 13.7 KB (13660 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:67728fb8e5cd3818b91715960c1bba0a0c0023bcabcd5671bc64df1d9df72da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31064906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f3f7d90cc1fbbefb0d8442ab9c23a806f90fef8b03dc4fdc5f1203b74992d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ARG RELEASE
# Fri, 21 Jun 2024 21:57:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 21 Jun 2024 21:57:43 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa83e4278dc6cff1ef0b2ddfdcdb95e8b576852125603aff18c4adbd62abfa`  
		Last Modified: Sat, 08 Feb 2025 12:31:11 GMT  
		Size: 3.6 MB (3594385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f206a367506b9a6e0da2a087a15345608f59c46aed8faaf14965a2048a684`  
		Last Modified: Wed, 05 Feb 2025 00:03:27 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d2194ff2bd3e4e851f237645c0bd78afd3a389c1df83bc989d3245af146c30`  
		Last Modified: Wed, 05 Feb 2025 00:03:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e4837f465facfb077234adc2a993e2a512c6e94506c37f467ca0d03c95b7d4`  
		Last Modified: Wed, 05 Feb 2025 00:03:27 GMT  
		Size: 110.3 KB (110348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9bb6e8c0c274860bac8c67b48375fd3b636f078b902c99d7683b178b98154e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2069364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54f0655895d6ff3d027802a83acd357d94c7309434a0a7690073fd3df7bb1ef0`

```dockerfile
```

-	Layers:
	-	`sha256:5d3714f689f360f18f642041f406b8692c6373b6cdc03d9b4e616e7686ccb86e`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 2.1 MB (2055579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ad1910f3d5ccf7f20eac6a6cb65c3a203059bb8a4456258e696ec7fdc164d80`  
		Last Modified: Tue, 04 Feb 2025 10:12:45 GMT  
		Size: 13.8 KB (13785 bytes)  
		MIME: application/vnd.in-toto+json
