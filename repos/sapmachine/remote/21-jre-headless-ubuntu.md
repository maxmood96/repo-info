## `sapmachine:21-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:1ae13689c8fe32140dfd023ada2e0d383aa8561ce090390f36a159ffb45d0239
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:2936606be752ed69a1cc5f697ce8ef1722ff80ce1db733fc0260b64b4b8f244a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88768713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b4c7491529272b301dae6414a1631abbed4ff01769bc2acee13afe2b7237e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74eb51687570f565bdb63c2740418aa40ecc84b9252820f1ddc3a725c529d6e6`  
		Last Modified: Wed, 22 Oct 2025 02:43:27 GMT  
		Size: 59.0 MB (59045566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:31979afef76308aa6b73a9a2fb88f722658d59e04c25a41b3c7b1e49e321dc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd7d9f691160375e88b77894765b9c181cf88f3a98a23f905162c95601aba84`

```dockerfile
```

-	Layers:
	-	`sha256:7aa94ca169b44725329ba388c5b4e6344a488791d981770da4449f94e9c87c54`  
		Last Modified: Wed, 22 Oct 2025 06:10:45 GMT  
		Size: 2.3 MB (2272810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2eb20f2b7f4c324737373e1b29ba39040441c24beb9d34a9f24876a41d26353`  
		Last Modified: Wed, 22 Oct 2025 06:10:46 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e18688dac16321f27d9c32bbf0507d634c71f2a787fa628d31bb9231683d39ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87087931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e21d4865cb2172e1079372ce7714cba4caec2efaa8629be5ef106bacd7865e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:38 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:40 GMT
ADD file:d77dea5c49828eb0de89439d2b631bc8ea27cb9ef774412b56a060ba1673487b in / 
# Wed, 01 Oct 2025 13:01:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b8a35db46e38ce87d4e743e1265ff436ed36e01d23246b24a1cbbeaae18ec432`  
		Last Modified: Wed, 01 Oct 2025 15:34:19 GMT  
		Size: 28.9 MB (28861712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cded7bef024237ec5089bba68d707cb343e7b6bcc31f3db8468e153cb36a5e`  
		Last Modified: Wed, 22 Oct 2025 00:05:50 GMT  
		Size: 58.2 MB (58226219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:48ea5930224d267616fab5c1f596abee64a2e920dd2c1c45038994b60ee72339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7873698da54674dd0adc79465089198a9c4ae57a314fee12de6e2f9b47546f`

```dockerfile
```

-	Layers:
	-	`sha256:c27238eb9fbab43bed2dfa08ff3e7a19db0a940a273c1c480e7f69a593a59d7c`  
		Last Modified: Wed, 22 Oct 2025 03:07:51 GMT  
		Size: 2.3 MB (2273317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3fba24c040499b20188de0bcf93aae4fc173bc3cb76454c484d0187d5dfa0a`  
		Last Modified: Wed, 22 Oct 2025 03:07:52 GMT  
		Size: 10.4 KB (10415 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:423611c56fceba0deae0d38eb34ec419f959c2c06f08bf44d9523a50507edd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94390374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743ffc13debad7bfac3272ff6589e581a494049362249d5d6a0f787fdd1e5cf1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 21 Oct 2025 21:30:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:782e7c13c586c2b237847a486d86be2132011c4cba7c3309595b3d2dadb4d329`  
		Last Modified: Wed, 22 Oct 2025 11:53:01 GMT  
		Size: 60.1 MB (60086849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:782943914ea5a5875980a4b1c914bf45cb625168a95c5c375a0cf8813c28b308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975971d40a8f909834e79b5706ab3219ac543ccd10ad9b8455f9a2578afd4325`

```dockerfile
```

-	Layers:
	-	`sha256:a71e14bfe05d14036df8cd2ca48b19471b3e4f7a9e7a1365fae916e69f1fa102`  
		Last Modified: Wed, 22 Oct 2025 15:08:07 GMT  
		Size: 2.3 MB (2270810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:260e30fc49d6e44ab5bde173ef2dbea6ae532e361fe03ad0d92b65aa6cabe6af`  
		Last Modified: Wed, 22 Oct 2025 15:08:08 GMT  
		Size: 10.3 KB (10331 bytes)  
		MIME: application/vnd.in-toto+json
