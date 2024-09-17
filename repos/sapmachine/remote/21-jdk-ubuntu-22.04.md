## `sapmachine:21-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:a7449c24ba32a7a2bc3d8dd165863412ea29c169b5bc9604708be13e413d3bfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:341411710593c55c3876002425721bd19c5f7eab5044df3fb89e05c3a7c80fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244749923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c0c9e64123557cf661059c85f964760527059a755623d24269a3facbc3dc90`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13160b1e2676a5eabc18a1a70b8ff4b82f967b62eaa0b4a6ef834a98ec3ce156`  
		Last Modified: Tue, 17 Sep 2024 01:01:13 GMT  
		Size: 215.2 MB (215214235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:32667124943062c0cb904e654025c63a0465cb3ecfceb8d1203b841f268ddf38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de94eb4dc98a5799c1c5fdf8661dd3c88a6596f74ac816369e7385ad9a1cd689`

```dockerfile
```

-	Layers:
	-	`sha256:32f33d1d316b0a17eeffb09f6521c864ba495d94788eea741f7e1c6a9d2533e6`  
		Last Modified: Tue, 17 Sep 2024 01:01:08 GMT  
		Size: 2.5 MB (2475042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9081e1378ccddea460fe56bc200ed6851d7db1ec6828c46e96540f10121ef8b0`  
		Last Modified: Tue, 17 Sep 2024 01:01:07 GMT  
		Size: 11.2 KB (11190 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:089e7f1e3deb957212f6006bbb65077b3cd1aa685cc66881988b04e110fd83d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240621224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9969812f9852469f8115c36a256cd363f2c56ee2b66ee2cba86a7f4e3c5434f5`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:97f62c0c00144d63b1be5e040800f0f0103e4776e510a4ecd9f36041588cd850`  
		Last Modified: Sat, 17 Aug 2024 04:20:20 GMT  
		Size: 213.3 MB (213262541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37b619f25a73e2581fe867ef9ecff996d4529cd65366cfbc5b629e51afca89c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2486405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9467e257caf895492faad342899fee6dbb41758d2557f10e9309a07ff985ac`

```dockerfile
```

-	Layers:
	-	`sha256:45142188b02d7821923f035c92fdd10a5a1bd6dfdd831d24140d671b1e21dc99`  
		Last Modified: Sat, 17 Aug 2024 04:20:16 GMT  
		Size: 2.5 MB (2474818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e98bae43da0570ccf682f4e80b9cea2d3aee60e9a1f5ba4ee4e49badf9b976c`  
		Last Modified: Sat, 17 Aug 2024 04:20:15 GMT  
		Size: 11.6 KB (11587 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6a19bd35adc13afaef0550090f0e015618867009d9dc55182f464e576195dbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (250990455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0495f2b780fdc14238a48af4bba4cfd3798b95bfc596afa3c1057e21d1b63d`
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
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254281285ede09901d5a74c4bf54fcd9d1f4e8579b68b9f00ac6221400f7f8ea`  
		Last Modified: Tue, 17 Sep 2024 02:37:23 GMT  
		Size: 216.5 MB (216542213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:45c49d73eaa1b800e4a3ff80549aa39a99af172cfc505ffc8080ca0a000551c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2488397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0ebda29dd8702efc6dca714ce38c9380f70845291e71a16099f34eccc5945d`

```dockerfile
```

-	Layers:
	-	`sha256:3f9ecdf69e686baf072bdea6c176f80f8c957ea22cdf0da4547de6c8a651d97c`  
		Last Modified: Tue, 17 Sep 2024 02:37:18 GMT  
		Size: 2.5 MB (2477120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036cfd9e05e4c4471d229bcfde2e4f12f676adfc92eb95af91cdb1d108cdf282`  
		Last Modified: Tue, 17 Sep 2024 02:37:17 GMT  
		Size: 11.3 KB (11277 bytes)  
		MIME: application/vnd.in-toto+json
