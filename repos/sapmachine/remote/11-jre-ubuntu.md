## `sapmachine:11-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:2a5a4442ecf6862223f84656f821adec11e8d13a6f2b8245757fa8fb2dcf02ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:e1e2f8e963935cb65a9a7e315c0c26f0094341eb473e4ba0f2d6775f551f0444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80102237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be26166e782716472a727b9e0082e665d5c9cff4a48dccfc52135e291e84539c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896732d33f4a0920780c38ece7645e13cad2ee9f695c343ef29a09702a0c96f0`  
		Last Modified: Wed, 02 Jul 2025 21:24:51 GMT  
		Size: 50.4 MB (50383871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1dc6ae2cc3e7ca31710991d23cae56d6dd468f4d1a291fc3f99f98570bf66714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2532468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219cb2df7122a09ffd8764d9177acaa07708eedba136379173adaf276bf27562`

```dockerfile
```

-	Layers:
	-	`sha256:8b271c52dbcdf87ba21d76503c8d96988ef1e4d1d42e80f838ce022942f80629`  
		Last Modified: Wed, 02 Jul 2025 06:04:44 GMT  
		Size: 2.5 MB (2522997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a101cc788f2b22555e23c4d0949b34adb31149664e30b4a5e99c68261150e761`  
		Last Modified: Wed, 02 Jul 2025 06:04:44 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json
