## `sapmachine:21-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:44c9e20c9a2792a82e935322feaf82d9814bee0b7ee1a816f8b82ddfe823e421
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:a5a3b469a1f8be0ae49cf8d7a3a2eb3eca9d7060975f3c17502f38ae1d5cfe07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243295703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8245f963aae4594970dea912e8b55fafe2bf766fbc429eade78f4d0bc39c0b3`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:44:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:44:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:44:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db0a63d72e28464d5080f3bc9e383ebebdeea112b980963639859a6e694a312`  
		Last Modified: Thu, 15 Jan 2026 22:44:59 GMT  
		Size: 213.8 MB (213759036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7cc8b5a83a65b77ba4392ae4f9a8b1589f5108dfc216fee60da686411955bc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9ed845d262e80496ce3d22b3abbfc02f6f04b5ad27f71de4d054238d9a23e8`

```dockerfile
```

-	Layers:
	-	`sha256:044075678bdaf6a508e032947441d97ebcd128cc2378b6894f27f29048dd6ba8`  
		Last Modified: Fri, 16 Jan 2026 01:11:26 GMT  
		Size: 2.4 MB (2377642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1a179d255555e5cd80cf8387ca13c53d9be468a04844709a1df181c6180dda`  
		Last Modified: Fri, 16 Jan 2026 01:11:27 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2ff63c914762e764e8ec6109a7561e0f73f59112ebe08a2ce0177ae090f47ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.3 MB (239341222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d7dbc15d96357b9a86c6b0342523b1b0ee103a1a65cd195791dca4d80b8677`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:47:00 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:47:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 22:47:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89b95bcb93668ae0b02839664027d97f4240b53f03dcc0a099df4aef1af2c60`  
		Last Modified: Thu, 15 Jan 2026 22:48:26 GMT  
		Size: 212.0 MB (211957725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eba462e7ccef61c77a79cc3f96dcc5a839cf1aa48f0156799a8f2966dad32f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45403e3ec195505ef2c76ed84b7d294dbe2accf80b32b58d3041e02323fead5`

```dockerfile
```

-	Layers:
	-	`sha256:99cea11ba8de8d15915d54392984b16ca42c266cda38e4e1cda3fc44b227d893`  
		Last Modified: Thu, 15 Jan 2026 22:47:20 GMT  
		Size: 2.4 MB (2377314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1daa5b1e4ad9bdf0ebe066c166674cc576d06309e40a44075c0f06d62cc2431`  
		Last Modified: Fri, 16 Jan 2026 01:11:32 GMT  
		Size: 9.0 KB (8985 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:114cd75a6090dd17e8eb58ef076ac4e4a2af9bcf753ba6288c36ffda747e8047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248870554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336b8b359943636286cba8b7b299e0579998076cb7f76593a6a7d1efb421a100`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:38:51 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:38:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 15 Jan 2026 23:38:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86123d490db9b8df16958a4511d4c520e811c0ef2a4f09bdbb8130eaa0ec846`  
		Last Modified: Thu, 15 Jan 2026 23:40:25 GMT  
		Size: 214.4 MB (214423592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ca54b49947fd69099f0fcb36a4a8952c32e8117b11a2de6774119521b27326bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406451f729562037c19dacef65dc9d28638bfe4c2e55df43506936e147a1666e`

```dockerfile
```

-	Layers:
	-	`sha256:60d3936fb1682ef714fc14e47288dc7f5b4dead0c9fa005079f3498d692120ee`  
		Last Modified: Fri, 16 Jan 2026 01:11:36 GMT  
		Size: 2.4 MB (2373721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df2bf530a13c042377129d33579251b066dfacaef81422bb143e1ae4f270d07`  
		Last Modified: Fri, 16 Jan 2026 01:11:37 GMT  
		Size: 8.9 KB (8925 bytes)  
		MIME: application/vnd.in-toto+json
