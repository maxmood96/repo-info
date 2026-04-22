## `sapmachine:26-jre-headless`

```console
$ docker pull sapmachine@sha256:44caaa492709c8fbd6b93cf933c8c7a14240a324ed60b121f48b8dcc4e1bee08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:304f20e40d150281e667dd52c22b470f5846f0937593400abba90db8c74194bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87557137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0f7c0f6f85d869c1dd4b9045343e0f842acc1cd0d2bbbb75a9062a58a31d55`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:02:14 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:02:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:02:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a29085bc660a3e496b02bb49068c67a481eb1c99d4ed226daab2c25947c51ad`  
		Last Modified: Tue, 21 Apr 2026 23:02:27 GMT  
		Size: 57.8 MB (57824159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6f08842586aade0bec18e5b77974c722813faff1900b5a5c19b53bef0184334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51010de1f2579ff96860d39a4bd7d1c8ca9fa66fdf16ef8b88cc1885dbe6ca16`

```dockerfile
```

-	Layers:
	-	`sha256:bfc9060eceea027c7570f0ce256421310b010fa9c538d647eed52eedf96f4b39`  
		Last Modified: Tue, 21 Apr 2026 23:02:26 GMT  
		Size: 2.3 MB (2280454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14213be6a8a3483de01bbe87a68d5275c7ad3b1cb14ccabaf39467baa880376f`  
		Last Modified: Tue, 21 Apr 2026 23:02:25 GMT  
		Size: 11.6 KB (11558 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f1451b2e262e22d7aa4e5069af0d9d00f96ba8d590bed7c83629c7eae821dec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85704994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281d2f0f1a4feda7fbd6b6f9c9201026708488443e7183620525bc9daeb32511`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:04:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be14a444da410717f2aebf5564c960e029c4e0684dbaeed17e2f86086adce0ae`  
		Last Modified: Tue, 21 Apr 2026 23:05:11 GMT  
		Size: 56.8 MB (56829209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e4cf8cc5d68d785aa182f6bd81dea993e0e357bf5b09dbea4450cebc6a265af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7289e4696cad4124666a13bc51379b276f6a48fd3b938d5e02ddf8fa25261ad`

```dockerfile
```

-	Layers:
	-	`sha256:356e0d6afc0b2aab5a3a4afa4373cfebc12341b00bdb591548d5d6939a2c8498`  
		Last Modified: Tue, 21 Apr 2026 23:05:09 GMT  
		Size: 2.3 MB (2281006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef51feb1a09ce2f83d184fa15061d059f3cf89b8135e742046e086661be55afd`  
		Last Modified: Tue, 21 Apr 2026 23:05:09 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:43d11b7b1526488ee51bb2630480e317de93804fcfbbb8c2e931ac4956405b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93104622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1075bf7740a97876a3c35835b76b04f77c282364ed4ea574d034f19662a4840b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:05:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:05:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea02f412da3992315a9860150b6442843ac38398592836aa43ca0bacac3a0e10`  
		Last Modified: Tue, 21 Apr 2026 23:05:58 GMT  
		Size: 58.8 MB (58790444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c5cde457cb6a88612e9e2cf2ac7bb9888c3066cf3bb8ad81ca55afa62dc5332a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2290915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59d657ebec18e7f476ad29879298a90110134a081cfd946592dfea6ea1dabe4`

```dockerfile
```

-	Layers:
	-	`sha256:6630fa9195324bc45324615c26c8716f13c4d54c5511ed84a335a91c208fd6e7`  
		Last Modified: Tue, 21 Apr 2026 23:05:55 GMT  
		Size: 2.3 MB (2279265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b67611bbde53687f17918c822f875d6f0cdd500bbfb24b7527fbe5d37b42de`  
		Last Modified: Tue, 21 Apr 2026 23:05:55 GMT  
		Size: 11.7 KB (11650 bytes)  
		MIME: application/vnd.in-toto+json
