## `sapmachine:11-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:0ed84152ac7fa6b0ac529efc20a60c056a72e050357af32f308eea6d778beac3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:84141ae163fbfc41a90ddc8a995dab89438798af84442731f1cd5c6c2dbea3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229188317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b80ae01233d3e96146613509b56d6bc3485b1094661c2a38c1c2cafc6319df0`
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
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
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
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277bd86b6f36f63d1c0ade3271307a09a6fc3664ce77b16fc6f3d5cba7bc2e37`  
		Last Modified: Mon, 05 May 2025 16:37:19 GMT  
		Size: 199.7 MB (199655703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:027259149b02665634a9f212813136d91c2f0bc0e4927f985c07718614f28010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2269332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3f6b6c4ab573c4dac61cd9de08cd87a9e7571e41d28018c1c99f4e551e6f8f`

```dockerfile
```

-	Layers:
	-	`sha256:23798f7cdd23be40c8dded053f0e074483e03fc41f816c89acf3cc64b0928b65`  
		Last Modified: Mon, 05 May 2025 16:37:17 GMT  
		Size: 2.3 MB (2260399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f493f311df4bc1c575389332f92963257d742f305a08e0b5572628704fd4b61`  
		Last Modified: Mon, 05 May 2025 16:37:17 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json
