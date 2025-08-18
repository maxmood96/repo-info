## `sapmachine:24-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:6b8f0335c38b8ce05eef4a9e2a757c1d6c7fb5a66a4695f6a7776a1022d82999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8c73ae850fa89dee200a391190eea636f309a271bd52972e4e4c5229f4d40c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261612400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65da5207a8a38acc9a517fa365cac4ee0d3268d46a254fb1a42d5c79151ab648`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5ffce53411be1a422be3deb099a242a292f18653819509ffec2a85d29fc935`  
		Last Modified: Wed, 13 Aug 2025 21:03:43 GMT  
		Size: 232.1 MB (232075407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d6962feb4d6f04ef0d4cc55d99aeeaa47f1cf6f9d0ce788c53cc501d9aaf8d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a182fe09035ed32fef99784cb5d761d5fb6ae87a155167a01dc8a5d1a294647`

```dockerfile
```

-	Layers:
	-	`sha256:4039732682296ef8ecdee6975063902826088a500d59cfa3f9a3b5eb7f33eb11`  
		Last Modified: Tue, 12 Aug 2025 21:08:19 GMT  
		Size: 2.6 MB (2621720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c8daa9c5f4336bce837badf21ade5e9780e9e3c14147ba94f81203fcd15bda`  
		Last Modified: Tue, 12 Aug 2025 21:08:20 GMT  
		Size: 11.4 KB (11412 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:26d7edf5867feee58c0005592bef11acc1aeb08a2d80908b7a24aedf599c60ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257322709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440c38f91d6f727757344a832950d60c63e900e84e8a129735bf65b65957bcff`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc54f3b8658a96df2592e3ba5f6032bba8058ce845f235e67a552917de5f4bc5`  
		Last Modified: Mon, 18 Aug 2025 14:52:29 GMT  
		Size: 230.0 MB (229963462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:81e5248dd5f50c5d4e081ee8d4708fe19a7b6498f8f2704ad84ef58b5d4e14a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb10207db39b1726821d0f13c1d36293a96b05faad18005dc65bc9fdc905212`

```dockerfile
```

-	Layers:
	-	`sha256:4d4795721bbf9cff20c94b111d3085046db88bc1eed9621baf172c4749884123`  
		Last Modified: Wed, 13 Aug 2025 00:09:16 GMT  
		Size: 2.6 MB (2621495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460dc98d3729fd7a7583a526c08cc643d68929f6e037e657e5f8befe0438d6d9`  
		Last Modified: Wed, 13 Aug 2025 00:09:17 GMT  
		Size: 11.6 KB (11611 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:20e2312d2a64d1f32e44e6c8227d58233ed557c3f2028748e274ba6d409e5f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267269416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a63c2b15d8acbca63e77107a9e97c54b663ef38f7aa1eff5d8d4ca7b3dfebf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78bc2a3142c6360821aec4973739da10d627c3fe083f241491be9f1f097466d5`  
		Last Modified: Tue, 12 Aug 2025 22:29:13 GMT  
		Size: 232.8 MB (232826271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a452084f6e559cdfc5801d23367900c9ad99049aa35dddd070ebd0044a1c7851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff59047c355bd2555b54abb04e8004337d2e4d64f504ddd4a4a409122c18f27f`

```dockerfile
```

-	Layers:
	-	`sha256:8981ff706f03b8de4927eeb9cf10503a8d454330d4c3df8e36567f7772594cd5`  
		Last Modified: Wed, 13 Aug 2025 00:09:21 GMT  
		Size: 2.6 MB (2617319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c8984804381cbc7c23d779b8766f53d5ae52be8a4ebe3ee3d795556d2f3045`  
		Last Modified: Wed, 13 Aug 2025 00:09:22 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.in-toto+json
