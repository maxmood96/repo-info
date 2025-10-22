## `sapmachine:11-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:cdf142162a82f8a842c7749ab0fe65564c4d2f7da7e5e3a9d00e117e83e01cf4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:e84d7c41443f22d99efa0cd5cf885411f72f4952c8cb4352ff0328383fc71f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228574037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5fb35f19a723078dfe12fc590b3e6e02898bea564bdcf42ce76214dbd09f18`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4e648682c406d5d9c14311d944c8adea7b49ce8b60c7bcb2c8a96537f902f4bf`  
		Last Modified: Wed, 22 Oct 2025 02:45:20 GMT  
		Size: 199.0 MB (199037219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb7f9087068ddf6c18c3466fffae73d0e880da68eec6af3d0cb3b0be2821b73e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e919bc74aedfac2297c6592ceff847fd00bd2dc4277b594e705af0f3aea0953a`

```dockerfile
```

-	Layers:
	-	`sha256:f86a7a46cb87fcdf3f4046c92a99bd1be73448f3b5f396c61882703fd6283ab4`  
		Last Modified: Wed, 22 Oct 2025 06:04:30 GMT  
		Size: 2.4 MB (2388507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf084991693680f68a55fa838c21db9914d94d1919d5a06b08bc9d6eb19387b4`  
		Last Modified: Wed, 22 Oct 2025 06:04:31 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json
