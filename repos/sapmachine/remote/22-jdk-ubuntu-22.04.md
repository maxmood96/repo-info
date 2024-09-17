## `sapmachine:22-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:44344b3252e900abeb689ed39904d62a79290b634ecb972b927ff5f94399bf2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:439044b020f747860a84bfd6e84f0b6413595321ccd86976a2a86a52fbe9939b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242765122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6acfc0c15ea1906037c4c9ccb6dd61640a123c336c88b92cf73f072871df386`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eca76adba4f0f53695167668998ff4880733e7aeefd6eb34ff94ce87d24a242`  
		Last Modified: Tue, 17 Sep 2024 01:01:10 GMT  
		Size: 213.2 MB (213229434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:869983d3c54190e85155b2cbcc03fa2bf60b809d33b4cff3339eec3051013755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55532cd8ff93dc0be107cdca10569109391a702b53a3b6f569b43726a7cf2d21`

```dockerfile
```

-	Layers:
	-	`sha256:038706b5c0f96406948934e822c607ffe2832d73a09c0261c5afa2df61dfe7e2`  
		Last Modified: Tue, 17 Sep 2024 01:01:05 GMT  
		Size: 2.5 MB (2475629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f24b3e4a8f06233bbb402ecf03063d255e29f8d32afee575b0bfa521a2731319`  
		Last Modified: Tue, 17 Sep 2024 01:01:05 GMT  
		Size: 11.2 KB (11159 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7bda4d8237bfbe563d08f1096912d1a520084c1e61e459a6b0a4567650902cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238532771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f7d51daad3da728eb6dde1f5abe78235ef8b0ed3bd767d26738c11fa5e2e6c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e4032fd778681091dda16ec4ff545d5a0a55a73b901de9c28c151e1a1de818`  
		Last Modified: Sat, 17 Aug 2024 04:07:59 GMT  
		Size: 211.2 MB (211174088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5a566ccb4edaea0397d5d3515942e54f06f682cffc7c8d7b7ff1f851b52c0cf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a71cfa5e359e59ef39d2a97970bb36d683b0a0962caf4b7ba4bec299eeb272`

```dockerfile
```

-	Layers:
	-	`sha256:feef9da764d522d0d06172b90c5ae9d74cc6d60bcf6d42aa052f773d04629dea`  
		Last Modified: Sat, 17 Aug 2024 04:07:55 GMT  
		Size: 2.5 MB (2474774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2864acbb66bd2b5796b288b56b37915eb04365107dae76288c143c6c157d29`  
		Last Modified: Sat, 17 Aug 2024 04:07:54 GMT  
		Size: 11.6 KB (11556 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b249358a4641102dc4b3cc781f29ec3b2aacdd99eeb9dd3cea7757a65c69d4f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248761655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5980b634cfae35f816736cce38526a67ae74853bbe26430314ce30a31a5ed11a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c942f4dd10bb2d5e51280b215c742ac06afc95c85a4bdcb6e8a97713e7663862`  
		Last Modified: Tue, 17 Sep 2024 02:23:42 GMT  
		Size: 214.3 MB (214313413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:29e928accd9b7d4eb4ee3adbfd337118529e3c65c9332912e86943aecfa19e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67bdfabaaaac8c429957156cb74ef119c61fd25faf2ad80e3a0dffebe62bd9f`

```dockerfile
```

-	Layers:
	-	`sha256:aff2358c51c25420dfdb9371ae3a54b31cd8058396010d7fae0c3fdb0ec738f1`  
		Last Modified: Tue, 17 Sep 2024 02:23:36 GMT  
		Size: 2.5 MB (2477088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7839c14ff363b2badfbe34b157ec2ae8cf10c13dfa0417ce3fdb09da7b0d16`  
		Last Modified: Tue, 17 Sep 2024 02:23:35 GMT  
		Size: 11.2 KB (11245 bytes)  
		MIME: application/vnd.in-toto+json
