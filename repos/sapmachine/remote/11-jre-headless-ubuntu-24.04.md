## `sapmachine:11-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2df6f8a5abe25f7139017670ba861e57eaafa72fa2d6631d47e18c071c469bce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:949c90503867ad8aa23dac53cdd2c228781c035b7dacbc7a603474be4009de69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78918566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a748adef42530d2e5426a2e9de9bad71638549822fe21ab4baa9c7518ab0a2ff`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cb57a1ee3681e77cef1afb710ab1a62afb5d6d63807b93dbcb230dcc3f443c`  
		Last Modified: Mon, 05 May 2025 16:37:00 GMT  
		Size: 49.2 MB (49201037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec0b19bd8c17de8299bc93cf87a3d72d90f21c01923247f88384e6f523009845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08496ec17f2f8b6b8009fcc7417526bab39766ec0dd5f6e3254f0148854bdd2`

```dockerfile
```

-	Layers:
	-	`sha256:905824954cdec5a69d1467af858aacdc706290319632999aa5563f3370ad04a4`  
		Last Modified: Mon, 05 May 2025 16:36:59 GMT  
		Size: 2.2 MB (2154718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b69e138075450a09271cce853f5c932edea9d227558f0aff3c2c87be5aa974`  
		Last Modified: Mon, 05 May 2025 16:36:59 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.in-toto+json
