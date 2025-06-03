## `sapmachine:11-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:61300f26f7d876b95c725cfca4069076c2f935617ce07ab0a1369fc32e57fe96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:6546ce877161e63885559ba994ddef1bbc3df146bf417b1478e65e03df5c810b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229188541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce7a13b75cfff92e9263d8c3ec0a64a904b9122ef407f6679837e0a827d1856`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c7cea6972461ccc755615edc96f5e1bbc839f01f807d198d0defaf8ebae95`  
		Last Modified: Tue, 03 Jun 2025 04:18:34 GMT  
		Size: 199.7 MB (199655538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ccca7025bfe6d7dece38e1a3a316c2179f31923093e8df6202022b69ab83d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854373ddb4dcc55927ac1aa8b2bd178ede3eb73c847a51f123a3e42afa72081e`

```dockerfile
```

-	Layers:
	-	`sha256:2aeee22c1495288616a0ad8d640dc4ae829d75500cd5dbdfa2121434650e3af8`  
		Last Modified: Tue, 03 Jun 2025 04:18:31 GMT  
		Size: 2.3 MB (2283479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a6e31750e542e7e008ece85e2b0b552d51458c03b4906659daa3b175907fb3`  
		Last Modified: Tue, 03 Jun 2025 04:18:31 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json
