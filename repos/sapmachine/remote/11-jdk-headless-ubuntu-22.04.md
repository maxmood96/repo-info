## `sapmachine:11-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:af4e2a1931e93960aa79204e8607d0321211d2b3f403463fad7dfa44782843f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ceb52791bcbd6e0e5b0d0fe70ba9e179bad037d03518cf65fccc45f1cf289753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229191246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3def7695bbf1268a15d2904980f9d7739c68fec05019daedafc7ee79d80bd1`
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
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
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
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0fae3ef886ffd76c2acf214a6c45f064c1a39242adcba249abdb64a39881e6`  
		Last Modified: Wed, 02 Jul 2025 03:13:29 GMT  
		Size: 199.7 MB (199655560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9e7b30ff37b06f5780daabd1e3a263e235cd851ad1621e93f5953a91bf4b05a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82492f9b0b87248077a5ba0bb4bb6ab00caaa603f1a1c6e0f2741689826b080`

```dockerfile
```

-	Layers:
	-	`sha256:933d0cbeda294c68b6ed2480168358e42b663587d0e1804d11720f528930265b`  
		Last Modified: Wed, 02 Jul 2025 06:04:21 GMT  
		Size: 2.4 MB (2388491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec23491a885ea5cfda3202cadab4169787ea2f08b2ce9f9b9eecb358c4823a9`  
		Last Modified: Wed, 02 Jul 2025 06:04:22 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json
