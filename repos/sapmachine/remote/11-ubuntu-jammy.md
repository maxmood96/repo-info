## `sapmachine:11-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:cda0fa730d6a5901cd0f7df1b819e925f9c93bc87f2376df183e93cb7ce0b9f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c26699fe9da4e12a68839e679d9cd591d530caa409a05a1bfcd1f8c209e011b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229790342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8197d1008acd0f7c6b7fccdb3be9f79567cb608d087f21670a19b12f2c34bd9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 21 Oct 2025 21:30:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf139dc5e17ff54a1b85bdedfd86d76e14dd8880bc2366814c3eabcc1616414d`  
		Last Modified: Wed, 22 Oct 2025 06:08:39 GMT  
		Size: 200.3 MB (200253524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:79cf229bba2bc89d46aff302ce4924e1bd7ffd07e11e9749e12421c383d981b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2650741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02784c61d81b5699230a7fab575232590d3f969e85c3664bf06e0b437effc5`

```dockerfile
```

-	Layers:
	-	`sha256:a73a7b573d7646458387e7aa494a1311f41d8eb9259250204c3c8a339718595d`  
		Last Modified: Wed, 22 Oct 2025 06:04:39 GMT  
		Size: 2.6 MB (2640603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b941e9f31bed51d30226769af896c2fe76704ca5652d98e0c78b92de2d84d909`  
		Last Modified: Wed, 22 Oct 2025 06:04:40 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json
