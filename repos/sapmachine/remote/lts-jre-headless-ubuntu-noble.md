## `sapmachine:lts-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:b485e5713388a8e7991d08dad03b0d3edf3d17691514213dc68aa8b8d8acd378
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:33ce151ffc77bca4e699ea1aa1f64a094dd0a44710f668ea08cf3351d5e292ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86287855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f122e3fc2cbf924e3fadafef14985581d72a7103765acd7fba3976e94f5479e`
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
# Wed, 15 Apr 2026 20:58:26 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:58:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 20:58:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4e3b85b364097d0645b732784f24cf609ac0de0bc3a15c7f69fd4b71663bee`  
		Last Modified: Wed, 15 Apr 2026 20:58:40 GMT  
		Size: 56.6 MB (56554877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e747eafb04dedabc04073a0c2c8635a4d80faf4fcaed8e5b5cab3d1b8e1ae686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1faac17180d97f627315032cd999bb70228a0804f33693da2b9891e99c26c20`

```dockerfile
```

-	Layers:
	-	`sha256:62557f3c8458349f0c59309710306ba358cca5a45a61cbe2995518a87cc684d3`  
		Last Modified: Wed, 15 Apr 2026 20:58:38 GMT  
		Size: 2.3 MB (2281424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09cafc2c524e0d4f9fddb6ddbe4e1ff5a7111bfdbc595bc61b818a412f39ce8`  
		Last Modified: Wed, 15 Apr 2026 20:58:38 GMT  
		Size: 11.3 KB (11263 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1c612ac3d0f5c9e3125a52a10df138e6fcc9e04bc1187b92979844876f45f50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84379718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f553704a4b5cd0f2bff3d4d897fddf8f219c34642953a00509c9947c3090c28`
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
# Wed, 15 Apr 2026 21:08:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:08:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 21:08:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a326fff24dbc39a9691fad1e837a8a900ee55fc9c459fdcda7b39ade4338f9`  
		Last Modified: Wed, 15 Apr 2026 21:08:25 GMT  
		Size: 55.5 MB (55503933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f9e9738296577fbf0c592db765b57a3c466729bd561ac36d2d0d51d47908ad5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb80646b1d241b3928bce3e554ebef5199a8427028c982be3630232960b49dae`

```dockerfile
```

-	Layers:
	-	`sha256:ae480445c4b01ead8f085a3c48b0f7b47c37605560ef7f20c3fe034734afde8e`  
		Last Modified: Wed, 15 Apr 2026 21:08:24 GMT  
		Size: 2.3 MB (2281964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:138c0b8263dda13da5dfe7a4fd49ca3c08060bfa551a5de813a5639014dd6372`  
		Last Modified: Wed, 15 Apr 2026 21:08:23 GMT  
		Size: 11.5 KB (11452 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:f5827b9b43bbf4b182a787657b363feb489b1caf9946c5b99c842dff8a48069a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91641094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd50c1cf5ad30786e996cee4657818b6dfd1ef17359752ef2289782107b717a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:06:04 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:06:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 07 Apr 2026 09:06:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18d1ece1ff4737346e83d90eccb531262fc08801b239db7f83dda918154972`  
		Last Modified: Tue, 07 Apr 2026 09:06:35 GMT  
		Size: 57.3 MB (57327760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2097f13d429b5db3dffe17bf7a290cb8d688b89d559cdbfc6146e2eee01d12dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fca19b9f4850087df2612ad811fd4b0dd7e2764b5faad6a368801fb33ea87ce`

```dockerfile
```

-	Layers:
	-	`sha256:eee25a3bdcba80bee9b40fdfde76ad2f57c5c22dcd9fd7fa255c5ea8f81c0e4c`  
		Last Modified: Tue, 07 Apr 2026 09:06:33 GMT  
		Size: 2.3 MB (2280229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75cd632d7c53b3c75929a4dfbf9ed77f924bd9be7a6a9da97d0bcc1f5e75e38b`  
		Last Modified: Tue, 07 Apr 2026 09:06:33 GMT  
		Size: 11.3 KB (11350 bytes)  
		MIME: application/vnd.in-toto+json
