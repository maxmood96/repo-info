## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:d0cac5872d95de56801c627cf98cc3667aca9a60168d1a2ff5d01a127c4bb938
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:e4711bf57fa5ebe876c984988206dcb88e02d048fb99d1acb854e18494325f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78316354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:235252380e5340bb9eed8b2b8933d37f3646116ae88124ce7570f4bbab898d93`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58804b82aa718f556785ba7917b156178da4b2b5d1188cbdca1c38dfe774bd1`  
		Last Modified: Tue, 03 Jun 2025 04:18:10 GMT  
		Size: 48.8 MB (48783351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1bdfe271ef97b0c19fef7d3f3a279bb9459fbae5a0c6e39691d286bfee4eb173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c815ead8aeda426f332ef61486a143a53a9d674d8d2cef62f91641f48ca66248`

```dockerfile
```

-	Layers:
	-	`sha256:8833d2dbd17e57a02fe865b3cfa96f93bbb9ee7003a26ab78b8acc9e9c58fe38`  
		Last Modified: Tue, 03 Jun 2025 04:18:10 GMT  
		Size: 2.2 MB (2194078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a97949d8da4f8a01a87c6b5ce67b6e9a3476dce9d354ed3727fc94cd8b95e9ae`  
		Last Modified: Tue, 03 Jun 2025 04:18:10 GMT  
		Size: 8.9 KB (8931 bytes)  
		MIME: application/vnd.in-toto+json
