## `sapmachine:17-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:fabd465f62f538c2473929b9fd69280b5c77f284dec4c6103e77981c3eda011b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:e90c83b68c05f34009842a143ac25617a03293f40bb40a3caceac32b39833b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.9 MB (83921176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b44e97903c665a27d23a4321cf29eee9812d66a26e3c3bc3c6bd3c91294f67c`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5697512ddfd3f5d73011e125e11b1b11ed815d996e07833cf52be016e28631cc`  
		Last Modified: Wed, 09 Apr 2025 01:21:34 GMT  
		Size: 54.2 MB (54203524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2a45148f81c0d48fed22ea8cda21481d37d2c9612f4036a6b115984d38709937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfd84bd63fda644e9205c3af137cc32b5e9fa5815cbbc61d717634747fc1ecc`

```dockerfile
```

-	Layers:
	-	`sha256:7136f74c19e00e2c5d5609990c726659aedae5dc31e2e389491f34ec7ecb6c44`  
		Last Modified: Wed, 09 Apr 2025 01:21:33 GMT  
		Size: 2.4 MB (2385580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ff885904d1037609ab21c872cb114a46c7f9829987cd981b2b152215b79b4e`  
		Last Modified: Wed, 09 Apr 2025 01:21:33 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:de7b2b6ff0a1a7935e3d0b625602a19bdb674e90d96cd7dde570e480a8916454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82501944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b270cef67f4c4ebd3d5dd9f4d04c3d8d89c9195964dd42b6242421202502b4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab991d9ccabc595ceb7b09df2b0e46eaa6abbdf2ef83b80031e18e2694cf7db4`  
		Last Modified: Wed, 09 Apr 2025 09:41:55 GMT  
		Size: 53.7 MB (53654986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ba539d9015a72713ff7a6ba3bb2e5b2ce4e580f46aebf8c3d21371b50c16b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2395670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6dc94481b07625c6d24d2637b1ac851d8845bdde6a457874e2c381f35eb5e61`

```dockerfile
```

-	Layers:
	-	`sha256:74497bb15cf5859bb8fe281938f2c7d665b6e77e11f7ba8639ab3c9e645f1ebd`  
		Last Modified: Wed, 09 Apr 2025 09:41:53 GMT  
		Size: 2.4 MB (2386072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81b8db4c909ee08e0a5785cff5ff8142505b18abe1f26472989ee5c32c75773`  
		Last Modified: Wed, 09 Apr 2025 09:41:53 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2614c63f622f78bcd5ed213cba0cddda5621f154b96d238895ef7f4da5b42d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90162330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f310005be4b3826bb5b8f2e53c72c661877c0a51b9b333ae5e62a33be35e1e24`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9761081afb015c16655617f0cd30c2b78cf5ff2862eee96962fbef895b54d4f`  
		Last Modified: Wed, 09 Apr 2025 07:13:02 GMT  
		Size: 55.8 MB (55821463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dca2205b1bb94cefd8272be79e6cde4a6d422509d38c0bf439d7f0e5f6226077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88273021968e6adc2d3a51661ea1cf956d375f00ff48cecbaea164aa7872432d`

```dockerfile
```

-	Layers:
	-	`sha256:8742ad5352b6ed883d574b45ae6842cd4321ceec7518e80193eedd4db51d3ec3`  
		Last Modified: Wed, 09 Apr 2025 07:13:00 GMT  
		Size: 2.4 MB (2389531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d2843b5e6269271f38ab48c822d184a1993fe975b4417860ac676304440f59c`  
		Last Modified: Wed, 09 Apr 2025 07:13:00 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.in-toto+json
