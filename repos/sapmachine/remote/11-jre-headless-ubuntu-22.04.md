## `sapmachine:11-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e89dd427246c5fac92daaa2bf4649fcf6a653f972f90d18fdf3a7add4ee89b55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:537f1fe1803549366d54eb7bfcee37c21ecc44822b315bf2c272e8c78dd779af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78335574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ff59ac0594c415b91d85a7cb7d009f2a2cfd64e73fadfc37881ced4e7a37e1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a6e601afa5f13f3fa688b6521ae06f018f4e123a7a79edb935f07a159e56f2`  
		Last Modified: Mon, 01 Sep 2025 23:12:13 GMT  
		Size: 48.8 MB (48798639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:70a17dfc648033d1e1a372e1bdb1fa582805e1fff355229c0fc5b1c36c9e08cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617c56053f5b09d007616a8e1ff70c9b15669e392d7122953966e726bf809761`

```dockerfile
```

-	Layers:
	-	`sha256:6a984869390dcf85d75cb29704ab3d57868f1aca515aa079067f8965e9ecbbdd`  
		Last Modified: Tue, 02 Sep 2025 03:04:43 GMT  
		Size: 2.3 MB (2299106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d03243a75e6890651ed0b55ccc10145cdf50474b3cd00e196db4d4091d68be1`  
		Last Modified: Tue, 02 Sep 2025 03:04:44 GMT  
		Size: 8.9 KB (8931 bytes)  
		MIME: application/vnd.in-toto+json
