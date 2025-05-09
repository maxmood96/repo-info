## `sapmachine:11-jdk-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:db7648de89187e93eb10743dc25e37a133852cda606f01ec8b2e6a5f2570c755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:fd491a8159fa752c1ec8d4efb6709d4cc5e5d4dc22064f3625e637f388a15082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227921731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb1888ec8d5aeaeb6e351ff8a4b8575b907c7fbcf96b4c8acbcbdc3bb4f75ab`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:675c6219dfa43d69c2a275110dcc6266c6548e7fd4ae7987433d4e5874d2aea7`  
		Last Modified: Fri, 09 May 2025 16:57:57 GMT  
		Size: 200.4 MB (200411337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:73db744be5d1edb69b5a844deb3a1b5349d451dd9a4df6121243e186aed10efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2406180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed88c07fe605b70819766c8aca004b200557d0712831b7efd0d108e92dfaa9f`

```dockerfile
```

-	Layers:
	-	`sha256:570bde64079de056c13163b6b17e2ffb4425ce4a4a0084636b1feff1569906ed`  
		Last Modified: Wed, 16 Apr 2025 16:14:34 GMT  
		Size: 2.4 MB (2396042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6445e6676db81f0245b2c3074a90c75d7f0a0fe46d7d0a9e277fce70409f2a9`  
		Last Modified: Wed, 16 Apr 2025 16:14:34 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json
