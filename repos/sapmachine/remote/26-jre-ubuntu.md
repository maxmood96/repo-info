## `sapmachine:26-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:d445c3055cebe5e8ee347c09f99f551ff8b79c259cd7cfe753ef57e96844eb00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:8e2b010fca30187ea221e551e13845507062f061b7ab245087e1a34b8175c43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88731731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09218bffc4e598fff92abb9cc1b563b48e520625f2f2324f08d6da4c6b3e758`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:57:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:57:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:57:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68df5bad7845d39328ddcb21e9b47043a3ce54c789f43ff550129180756bfa23`  
		Last Modified: Wed, 15 Apr 2026 20:57:28 GMT  
		Size: 59.0 MB (58998753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fd487550d2e69fdea9f5d2c2c6fec27380f8e42766f6f96009507f20b2192c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2534817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c747c8c24c648cc36a1a0c6033c28ccc63ed70ce11bc26e2d4ca2a21a2f51c2f`

```dockerfile
```

-	Layers:
	-	`sha256:23140458874cb8f55853334bd129b009c0e86f35ad91324987ccb3fbd873d714`  
		Last Modified: Wed, 15 Apr 2026 20:57:26 GMT  
		Size: 2.5 MB (2524848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec59b53f8eaae745f98bba66e9bc5d2e96c58c3249ae6dfb25e2ce27279c49b`  
		Last Modified: Wed, 15 Apr 2026 20:57:26 GMT  
		Size: 10.0 KB (9969 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d3a46ee8b81410072fcaace8daba97e5eb616d071fb3319b7886136e481550b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86882662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3982ff1bcab5e2b64b87d388ef5e48c788ee82e1666316718c53431f1454a8d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:06:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:06:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:06:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd4f9c792f8ff47cc264215f532e24647d0971ea8f70cf805abaa05d0f4f975`  
		Last Modified: Wed, 15 Apr 2026 21:06:30 GMT  
		Size: 58.0 MB (58006877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:508332f60989bb624ebaa87001e1083fb8d378ab612002ec1702b16ddfcbc6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1181627367536a891a87cf3bac923d35b264361f3a1672b77c081d1797e3e29d`

```dockerfile
```

-	Layers:
	-	`sha256:e4b64f26bc08694c0937e2705030e6a5c0838000a99e1b58baf2b3bd54acd6bb`  
		Last Modified: Wed, 15 Apr 2026 21:06:28 GMT  
		Size: 2.5 MB (2525361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b108430ec9d044a8def8db52df446590217d074c3c612e2f8d97b4ae978c3ff`  
		Last Modified: Wed, 15 Apr 2026 21:06:28 GMT  
		Size: 10.1 KB (10121 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e20bca4fcab392b13349d0fa7fa55a75f040b0da85cee603d16fdfadd52c7df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94471786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e98bc1588bd3bf3566dc891bbb20a026d18fef8bd7f3acc607ef871d062b76`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:21:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:21:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:21:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eee52c7998af13697c25bf3114d1678b4bcea4fe8963c8bf2e47efb720d029f`  
		Last Modified: Wed, 15 Apr 2026 23:21:38 GMT  
		Size: 60.2 MB (60157608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c520c9a698c155de84f7003a2f3b2f01c54171d33e846e9859b32af5d6a32784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e511d28df9d9aba36e30f5c807f454109f57a12704fa3eb00cbd4ae9eda89973`

```dockerfile
```

-	Layers:
	-	`sha256:62abf0617c603b32365be4e9efdba9ce587452582803d74f89634b7969dd3581`  
		Last Modified: Wed, 15 Apr 2026 23:21:36 GMT  
		Size: 2.5 MB (2523716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99d74cd0d8c8eb5f32891eb4dd6c989b2092ff8dc442e20587544cb26f5b2c74`  
		Last Modified: Wed, 15 Apr 2026 23:21:35 GMT  
		Size: 10.0 KB (10037 bytes)  
		MIME: application/vnd.in-toto+json
