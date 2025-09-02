## `sapmachine:lts-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:08ee8f87ab4784645f062f0b19fa0ede1dddf966ebe69ab3a577fd41bdbf2d98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:52fcce69cd31aa23c9cce3c127c1ac12ee41f3581830c6254f8bf8d1e378db49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88133805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3192ed4358a3c2259190af1fc443c5b94755c89bc2197327af6973abacdfa29f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b5aec6e2f3448b04da55ce8dba88b1c9a21adaff1065d50b8852b0efcd47b5`  
		Last Modified: Tue, 02 Sep 2025 00:24:28 GMT  
		Size: 58.6 MB (58596870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aed0219ec3064547db82443c691fe7a0c5cd3209abd7e7722ba37ffac07ea847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979606cbcd0412a73445a392ebb90ce993502516db50598cddf7fdb0002d8ce0`

```dockerfile
```

-	Layers:
	-	`sha256:567d41abd3b58e03ae7a44c527f30e8c0770cc31ab9fa9164d6f46a1c29ed49b`  
		Last Modified: Tue, 02 Sep 2025 03:07:53 GMT  
		Size: 2.3 MB (2294813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9172c0fd7e8ce04aa3049256ba5a2913e9b0dffa04f455007fbfdef9bbf404`  
		Last Modified: Tue, 02 Sep 2025 03:07:54 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:901fa46efe678e5dc47b3209b0df93812e403e876433103b3061d436c2b960f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85087844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8ce7f7aec7139d2d89d1506d2c8ecd9168db04cc9684e0728859877db82572`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2390630ed23d92d1d708585acf72e3ac74de535943bb62ea25bdb71cadb72f7d`  
		Last Modified: Tue, 12 Aug 2025 21:29:04 GMT  
		Size: 57.7 MB (57728597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b1a4f91f1540b6abfe398b01b181b67f97e728ef3839a63e38fcad002cabfc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3188abfeed577a98a96e1535bad95de2e8536eb30b7a12c72bc91762d2c94f5d`

```dockerfile
```

-	Layers:
	-	`sha256:cdf8556dbac06e73c87c212f977bd44f8b399886f5b812d135a15babe2c8234b`  
		Last Modified: Wed, 13 Aug 2025 00:07:38 GMT  
		Size: 2.3 MB (2294493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea762b34722d91cbf5cc9737186a3ced100c0992a0c36068b7726caa8211e78e`  
		Last Modified: Wed, 13 Aug 2025 00:07:39 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:74f995f1b78fc2a59d912772a815e7e572723ea99a2baf1b521000440a087e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (93988450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d55a98257bc2e43bbd21bc5bfb643bcf2d7cff81474083f8ea1ca515e18957`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5823897770ba5cb1fe37e29288eb3cf506c2eb6b374fdcaec36dfd048ab698`  
		Last Modified: Tue, 12 Aug 2025 22:49:46 GMT  
		Size: 59.5 MB (59545305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e4eca57d8230eb51c77308d00b3832652f61eafb03ed4ad3ea0128a6b859a872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b65a88d24d7b653c3f60ccc9665c61a81a174eba2d2e2e6fe7ad9db50ae1fd`

```dockerfile
```

-	Layers:
	-	`sha256:ae79b17d2883bb8d0a0f3288b7659e67ee5858eb5cf63a6aac271ee9f15b3ace`  
		Last Modified: Wed, 13 Aug 2025 00:07:43 GMT  
		Size: 2.3 MB (2292834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c496242b3f1e34e5c8d6d3cb52fe15db06b5257ae01b52488d2d30c9c0622152`  
		Last Modified: Wed, 13 Aug 2025 00:07:44 GMT  
		Size: 9.7 KB (9682 bytes)  
		MIME: application/vnd.in-toto+json
