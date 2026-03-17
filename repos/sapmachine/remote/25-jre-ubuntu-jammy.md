## `sapmachine:25-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:d1992a512004c5825f9af32db0da4f7a06dc6d8a50e55933a397b00f5490ed41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1904bde71f4d4db577396ba34386562032a9ebbc0a7fbe014c9edabe63aa4d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86885291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073a4521b37efe0206bc1c7cff0c2fdf394ebedbb0a93dbfe11a6bde72adad9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:24:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:24:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d07faf37dfc7bfdd3ed631b9f81b6b5fac38081defda59abb566566497678e`  
		Last Modified: Tue, 17 Mar 2026 02:24:29 GMT  
		Size: 57.3 MB (57346771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08688f26ac1ec21936814a4cbfc4db125b76981c699e27563bdd1b6fd97fb386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2563822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be059ba6c716639d306d6ff3f3851ec598cd3709f0930e2b4e921f29649029b`

```dockerfile
```

-	Layers:
	-	`sha256:1a61e2290933b5bff96e9b40983a333c036449e3a83dc327c70394967fc592dd`  
		Last Modified: Tue, 17 Mar 2026 02:24:27 GMT  
		Size: 2.6 MB (2553733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d650eb21eba8f450bdf47a4a7f17816ae5fc358c205d4bb9b4b35cd290ea398`  
		Last Modified: Tue, 17 Mar 2026 02:24:27 GMT  
		Size: 10.1 KB (10089 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5ab0afb449cf57203e8a8d261cb2317e34790863095f9ba1fc334c3ad3263887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83650225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9559210f71646c12694b3d1583d835b6fbc2828c1734904091be7f33ded53e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:30:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:30:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:30:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3ea48eb5bb9dab6fa2dfae6ae630408ac3535e604c76e7403f264b9aff8e23`  
		Last Modified: Tue, 17 Mar 2026 02:30:17 GMT  
		Size: 56.3 MB (56261200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f7b24629de70b88d096466924eec71753ca09dfc4a7dc476f4411cda77dabda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2563701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed6c8bec19426208c7ffeba28146089a118ad2c3b9dc7aea1122bb5ec095e6`

```dockerfile
```

-	Layers:
	-	`sha256:042b7cbd0cb5851802d3eaa64bcffe558adc036f85ee860d9833879a8cb9a623`  
		Last Modified: Tue, 17 Mar 2026 02:30:16 GMT  
		Size: 2.6 MB (2553460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d27543941d89ebae6014324336d4080c2938ec64cef88d853074462f1bcaa1f2`  
		Last Modified: Tue, 17 Mar 2026 02:30:15 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:daaf076bff7b8748e0810f6accc4c86db82c5e814bb6339fdd32e3e7986c9d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92669898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cbcc563d22476655172ca696007ff7b1fabe347535d0681e222bc7291c5931`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:24:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:24:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:24:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6c1a4c1b70b04fb1b27dc8da8fc75f84f026fe232a9a76b9874e408d2f38cc`  
		Last Modified: Tue, 17 Feb 2026 21:25:04 GMT  
		Size: 58.2 MB (58223796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e01a9624c987b95a37923faaabe3dfda21b1b27c2881ec914ee03fc6faad2f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c5950041c1983840b311d30cc67f0c961eb340d49257ba06731ae82c05a547`

```dockerfile
```

-	Layers:
	-	`sha256:bc229fdd13fabc4ef988b49c636b7f99f59217a6aa507a36ca5afb2ae961e15d`  
		Last Modified: Tue, 17 Feb 2026 21:25:02 GMT  
		Size: 2.6 MB (2552659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4450825de2d7effa15b8eb9f675a793056e866350060d1144a9c006c4babae32`  
		Last Modified: Tue, 17 Feb 2026 21:25:02 GMT  
		Size: 10.2 KB (10156 bytes)  
		MIME: application/vnd.in-toto+json
