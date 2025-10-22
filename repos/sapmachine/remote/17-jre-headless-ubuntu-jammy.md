## `sapmachine:17-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:827b33de02f6a8666bf4a17c5231401c1bb5941e48517af622a3d5f766ee8dac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:23362cbca357182469c93afc660df38600f848f735d6aeda56f8d4e756e0a509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82255267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b952252d550e58fb74635e61e1069ee31c16fc58ff439307cbc696404860c687`
-	Default Command: `["bash"]`

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
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b42373470b1ceb7b204439825c2edddfd9ff28033cafbdc38ecf4363673d956`  
		Last Modified: Wed, 22 Oct 2025 02:44:32 GMT  
		Size: 52.7 MB (52718449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3998f477fe18d82c32a5b7970ca84679096db8dcb7b627a55c39992a27861d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d825f2b0df19bcd02c5a769d1b825217c107eb0bb473025fa27fc206151d03f8`

```dockerfile
```

-	Layers:
	-	`sha256:73cf6e1472a2e13646c3de2f48b72bf89eae4d303bb6f26f04bf892020cc053b`  
		Last Modified: Wed, 22 Oct 2025 06:07:34 GMT  
		Size: 2.3 MB (2292859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175bb4861d8a9686ac7b0b0723138f86446334f8b1aad9d23c598d20944b78c3`  
		Last Modified: Wed, 22 Oct 2025 06:07:35 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:02c2f80f81ae40d082a70c0044c255fa6cd5abfd6b01d836a2c7f1083d7c8807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79475946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f701fc842bc42abe40a4610ff0b73357ad57cdcd57b89e32e85505c36c777c68`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddd1286b773ac266966e16756e954d6da4b2f9aaf39626d05af66f3d17ae5b2`  
		Last Modified: Wed, 22 Oct 2025 00:06:54 GMT  
		Size: 52.1 MB (52092839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:200cad9bcb8d5b70860a261312024d825d7c73ad7823eb06534cadc9f7a86f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0fa9e688aaaf76e0ad2f074a44fa0f835a81dd2bb9bfe30121fa8abb761b45b`

```dockerfile
```

-	Layers:
	-	`sha256:ae34dc90580072f16ef54d32e1fa8f84d378cc689e6ea3f6dd655a0702d06735`  
		Last Modified: Wed, 22 Oct 2025 03:05:27 GMT  
		Size: 2.3 MB (2292531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dd6b2588d8d395d0d86f678d1a6b337f42ac94c4a9a35e409f29371696d676`  
		Last Modified: Wed, 22 Oct 2025 03:05:28 GMT  
		Size: 9.0 KB (9032 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a4872b9b460f47950a7db3872e5a627af5c6d27e94dd58554fd87030f5ec2883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88079090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f16942bf5ebbd3dde706629d3fa90f7e2e35f84f0225850e5a9be403dba8a48`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Oct 2025 21:30:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:644e04c7f00a6f70b0dae5798b639a1d8c498601a6840aa8026c2298921bc8b7`  
		Last Modified: Wed, 22 Oct 2025 12:17:36 GMT  
		Size: 53.6 MB (53632301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:57bbec7b864eef64411d13b76ccff0fb19068fe5ba4c9544a38f25dc4d262d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f146fc12e56cc47c7856b4b395333a6d09c66348aef3fc92c0c632bbf8ad97d`

```dockerfile
```

-	Layers:
	-	`sha256:19421f94990b61d1418b79bd54530892bb895b4940e5685e2f7801c6913c9af3`  
		Last Modified: Wed, 22 Oct 2025 15:05:34 GMT  
		Size: 2.3 MB (2290884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c622e80f13a1d3e9cdf1995842aa211c542590015fb000ffb54ca958bc194b2e`  
		Last Modified: Wed, 22 Oct 2025 15:05:35 GMT  
		Size: 9.0 KB (8972 bytes)  
		MIME: application/vnd.in-toto+json
