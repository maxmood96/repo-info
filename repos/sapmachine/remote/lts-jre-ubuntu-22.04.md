## `sapmachine:lts-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:1aba21ddbe0c8fefd9bd08a3d73b15d6f3da11356d57db57931484969c71be32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6b5bee68c40ce90acf266a2e669431c720f2017c4bf8c5fbeda8bc8c5c805946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89475800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722c2ec16ba1c6a7e398ee7281a058547024d18a88d43626f316d8a9e75a3d47`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:2f8a54a5efd080fb81efea702b4e3e07d946eec7563fb2281bd28950c10ec462 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:857cc8cb19c0f475256df4b7709003b77f101215ebf3693118e61aac6a5ea4ff`  
		Last Modified: Tue, 13 Aug 2024 10:44:49 GMT  
		Size: 29.5 MB (29536025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6403c3b3c1e6678b63fe1cea6dfdf78d3dae56f6c06f3f62d9307c8b1952b0b3`  
		Last Modified: Sat, 17 Aug 2024 02:05:36 GMT  
		Size: 59.9 MB (59939775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6d441316789e35c115d7fbe89d1c72db1e71a0cd7690833e2cbfd0b9083e9ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadd527aa9d79af56cfc04da8fa9182e762df246ba91bb17f632e90ee2b9223f`

```dockerfile
```

-	Layers:
	-	`sha256:fb6c510583e8355b95df227305d5fbd98a00ae5a9f92f466b3667f5fdf41bffe`  
		Last Modified: Sat, 17 Aug 2024 02:05:35 GMT  
		Size: 2.4 MB (2389425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ab320628dc78894994a5c4c3808bd8ee230ee4ffc6ba28f7eb2beb1cc12e8f`  
		Last Modified: Sat, 17 Aug 2024 02:05:35 GMT  
		Size: 9.2 KB (9226 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:adf49a1e4343d480b596b28584c226b95bc40d97cb2e69224ae5a7f3ec793ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86356009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e35aa4e009270c18f718980ddd7d18fda7e96438f4c27f018af9100fd70ec8c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c954a2e37a3febe379ba5d63e5b5945fe45200c62c945013df132472e785c51`  
		Last Modified: Sat, 17 Aug 2024 04:22:25 GMT  
		Size: 59.0 MB (58997326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7e22dfb514e539b443f5ed63d1f0a7fe54ad9809f4ab052884d121da452a803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e187232f001e3af298f05773b341e5bb8a49da3d19bd97b030c91cac869c2547`

```dockerfile
```

-	Layers:
	-	`sha256:153073c0493fca4b006efb4f69fa5d285c5d34639ada867340e7c229d3b2b376`  
		Last Modified: Sat, 17 Aug 2024 04:22:24 GMT  
		Size: 2.4 MB (2389129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2767e2b7e505d0a8cb27c06728e8aa4596dd7469da4586df6d85afcfa61d16`  
		Last Modified: Sat, 17 Aug 2024 04:22:23 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:08cb316eac66f641402a7855d5477c5b78011c3dafd9c795be285a3552259fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95967324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06754706b2d25def5d3fc609ee8483a6c8f0c8589bbf49bac89b69718e7855a0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97d2f176e88c7aa09633d044d375a8d0e71f8905deae118ab3621f15cc1b4c2`  
		Last Modified: Sat, 17 Aug 2024 02:56:54 GMT  
		Size: 61.5 MB (61503146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2c7d3c236ba05a0834699c2ca772507bca3843e39cdca35a800be57f4ec68be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546da36aa7d4c0eee0e99ff5e3c26651ec2b6de9590e526ae09a2d1ac854e943`

```dockerfile
```

-	Layers:
	-	`sha256:ff7921d3a46e6ed0ab922f13da69d98b393da5df582b58a3bdc8da701630144c`  
		Last Modified: Sat, 17 Aug 2024 02:56:52 GMT  
		Size: 2.4 MB (2393416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2cb292e2298bdbb42a43714b28c746f330a10cd9ce7643d3d055f4f991e971`  
		Last Modified: Sat, 17 Aug 2024 02:56:51 GMT  
		Size: 9.3 KB (9276 bytes)  
		MIME: application/vnd.in-toto+json
