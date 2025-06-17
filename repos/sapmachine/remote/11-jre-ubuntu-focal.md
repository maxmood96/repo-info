## `sapmachine:11-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:d67aa48ce71db37b40299497e979930091fc3a815850939518c7bdfafacbaf43
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:eec094b275d0de7be259451c839158b2d3bdc94c9398e1a882f671abf941df59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77053926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c00860d1bed6b2a1aa398cf918547266bfda70beeb3160e8efa7c01b0e12f4c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f642a871a1868bb0ba5812932cb1429111faf583dc80595cbfeb36f97752003`  
		Last Modified: Fri, 09 May 2025 16:27:46 GMT  
		Size: 49.5 MB (49543532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d4cb917f778d435f102bc80ecd4a83f46e7b15f13ff5e969b7437ca968eb7e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2314145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58b401e2f74e3f9d0f658aed5809b9184c5b6a4abc93365e0aa4d21a1b36530`

```dockerfile
```

-	Layers:
	-	`sha256:8a71be4233939e494dc50b58a17a92a33691d292ca0ae6f8c8ceafe3f1dced12`  
		Last Modified: Tue, 17 Jun 2025 10:28:09 GMT  
		Size: 2.3 MB (2305325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:900cc303d5fa03792012b382b25b884604f8392fec0f37eec7e00570ecb111c2`  
		Last Modified: Tue, 17 Jun 2025 10:28:10 GMT  
		Size: 8.8 KB (8820 bytes)  
		MIME: application/vnd.in-toto+json
