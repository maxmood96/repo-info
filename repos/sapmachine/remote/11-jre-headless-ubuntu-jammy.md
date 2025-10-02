## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:44618d47038e73963100f1716c7205f9e26ee1383a7dd0f29f2183d16d2c456b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:74b3ffbfbf0b1333786c65025c58dcdbb95ade4bece1f10bf184ef649e8214d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78335572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bae53d2947e32844da39337ba9148e8c53908498c09bc01105abf2d28b9e53`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:39 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:39 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:39 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Mon, 11 Aug 2025 06:09:39 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 11 Aug 2025 06:09:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583548e0c78ab1996078d15aa8ce010bd3ef24e973bd085d4fcaba2f1edea44`  
		Last Modified: Thu, 02 Oct 2025 05:21:03 GMT  
		Size: 48.8 MB (48798754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:418611cad34b52cf0e336042b54bff83c170a2039a6e3675549e92c99a4a9da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1957299abc7f7b4258d0329d3262df71638211b5222df3a01a1ca8f9191e2dbd`

```dockerfile
```

-	Layers:
	-	`sha256:4cb9a8526c768161a76f9241ae7acfdc564792ecd0e814ae3314b68c44ec66b0`  
		Last Modified: Thu, 02 Oct 2025 09:04:57 GMT  
		Size: 2.3 MB (2299106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07f08e71b7f6dfc5651041881e093d8f614511883e8456e4962c8e31b9868a1`  
		Last Modified: Thu, 02 Oct 2025 09:04:58 GMT  
		Size: 8.9 KB (8926 bytes)  
		MIME: application/vnd.in-toto+json
