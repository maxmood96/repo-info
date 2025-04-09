## `sapmachine:jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:ee334b110e319f3134ba2be21a22044b3daa11a97e742fea658d716d31811c8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:5b34ec6a1c2b21a2f6cb7a335edf9ce0e76efb7ca0d31cb79837b62b11e2597f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96583669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0baaabcd05922436af7246360a99c46357a9b63cc8ebfe3b0cbffc862e0c327c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d498c18cb0c08d6e0deebf8fce17909254ed1e3235e754f45a5e58d7d49ee3`  
		Last Modified: Wed, 09 Apr 2025 01:20:33 GMT  
		Size: 66.9 MB (66866017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b65b308f558d3fdd96978346f0366c4e0af7554349aecdc8e4a222f7c7aa4f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c952bc7e7d58f7c40bcc8a8c555ddd673aec2a0f105e1a47b52446b2f0d5e3b`

```dockerfile
```

-	Layers:
	-	`sha256:e42543b827d3ce71e5b1cb02f7f38c75f7f018312b5eabddf3dcfc0628e91848`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 2.2 MB (2156934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed72415e6f8a3721d4d074f496b10ec186830b4d5b960f218695f46085c0c7f`  
		Last Modified: Wed, 09 Apr 2025 01:20:31 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e8afa10c90a7874914883126cff7d303f69933137f509b8e609c0f05898989dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97016652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b601634870fcd1091bb1cf4720a3403a6d514a472a13c5b18a6f6aa60dcf2680`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39381959dcbe23635ea24af176e6a81805f3abf509d4a71dcf75d14ed8cfe5a8`  
		Last Modified: Wed, 19 Mar 2025 20:35:25 GMT  
		Size: 68.1 MB (68123054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:35c275ac67787ea82b5e05b56e2c233d54fc8477361dd9374ee4ae63e909ac5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2169318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab409ff58fff07e47ed6f06391d5cb7195a44bdbfb3722d5cdeeb531fff5bf85`

```dockerfile
```

-	Layers:
	-	`sha256:b780c6637067f32abd2d28e2162f1abe90c206ca8e443d9f73807ff1760816fc`  
		Last Modified: Wed, 19 Mar 2025 20:35:23 GMT  
		Size: 2.2 MB (2159633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97f6fc76668a1084c0ad0829b9b299d426767651cae42d2e362723119fe340a5`  
		Last Modified: Wed, 19 Mar 2025 20:35:23 GMT  
		Size: 9.7 KB (9685 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:35ef2511fddacf059b8cf948bdcccf69723a18426d7023f378f90607f61b7523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105063527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9028351111321824fca737a933736c3daaca7469aae272f80b2d3e4586c6c437`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f035eacba8273898515046e09c413294459618536a2e2064b2163c459698eea`  
		Last Modified: Wed, 19 Mar 2025 20:53:27 GMT  
		Size: 70.7 MB (70673703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a1fb9fce8b84ec94aab349982c9c473f241e34a6204c4ec40d4ede06c651f140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2172024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a6742b1f7ba4987bb8ba7ed962f24e3c60034a1d1c165010f9114031a0d25d`

```dockerfile
```

-	Layers:
	-	`sha256:fb9446e0ba7b42d7cce83bee43e66441e68203fc568c16cdb33aa82013b90eda`  
		Last Modified: Wed, 19 Mar 2025 20:53:25 GMT  
		Size: 2.2 MB (2162411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c262d73c4e29858317737580441a0b0c7703d02f7224126c00eea5084da82db`  
		Last Modified: Wed, 19 Mar 2025 20:53:25 GMT  
		Size: 9.6 KB (9613 bytes)  
		MIME: application/vnd.in-toto+json
