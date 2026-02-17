## `sapmachine:21-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:4f6d15934eeab8a525075131b5a34f3549ae9baa4d92f2a8d37eba82e0492e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:b4f04ae405f5d7eae575d66558d3145bd6ee0a45be14ae2193f681341c926092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88614532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45eb2b32a9ce92427023e1433ae3c6ac3e70f49b1835373417278eb2d114426`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:34:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6715ef8fa59330abcb93d87a99c3319028fddc04225c5ecc5b40fdbef5f2ca8d`  
		Last Modified: Tue, 17 Feb 2026 20:34:59 GMT  
		Size: 59.1 MB (59077166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ef180ec7c328e59cbcedb1add7dc221224b5e4a8f5a7d4fa6c954c1ff549c76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8835b308f8501b3fdcb801e1e94273b399086dd2713685a19a679d83421671`

```dockerfile
```

-	Layers:
	-	`sha256:8453edacd5e54b11a5a8ed0e39599b2635b3dedb166b791f6ff4ab4cf5ed3774`  
		Last Modified: Tue, 17 Feb 2026 20:34:57 GMT  
		Size: 2.3 MB (2296505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d406a26e5c1b03de3ccbf05856a7d174c9f58c374250bbada7ff1ca0543d217`  
		Last Modified: Tue, 17 Feb 2026 20:34:57 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:673abf92d1f4324efb55c22a899ccc45dc096123b35fd26437b11da6fc97e68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85597024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7d8932bcd3db0f922e53121f907f907702748845d655c4c942fb705804c4df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:34:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:34:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 20:34:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c822dfa5ed5234d05e00313cc2ad3f2327a86c59cae32cba0bb027236c2817ab`  
		Last Modified: Tue, 17 Feb 2026 20:34:20 GMT  
		Size: 58.2 MB (58212080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fbc9eedcdc8d637a4c9e6727b87327eaf73bb55eee46eb9b8a1e0f795a030519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e8e770bf060cb35d49c1bc03d5b8b52eb479554d32e22b49d200349c35447e`

```dockerfile
```

-	Layers:
	-	`sha256:40e447cff072131b7c0d6bf8a553e4ecf53bdea8c63ea10f8a8e636a3245785d`  
		Last Modified: Tue, 17 Feb 2026 20:34:19 GMT  
		Size: 2.3 MB (2296177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:012c96929da829f91ec0295a5071a7b0a8928b901c98491fa4c7c193e7abe972`  
		Last Modified: Tue, 17 Feb 2026 20:34:19 GMT  
		Size: 9.0 KB (8988 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:619c00ba842b78c41d186471c05609d494258f1c262d0ae2093e098ecf163b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94548443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897c427e390bd23e819bd514e84dd45138ac8fddb0bd65fae8767bac8ce0f0ef`
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
# Tue, 17 Feb 2026 21:31:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.10 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:31:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Feb 2026 21:31:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f76d557871747fad8dfdbb7d9bd2fdf375035b263f4d48fb5de1f9820cd1bbc`  
		Last Modified: Tue, 17 Feb 2026 21:32:11 GMT  
		Size: 60.1 MB (60102341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:490d131495b77b7660adf6c8b667f26ed6b860a866ab3fe859239da727ce4a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4ee2b9f8ac7c7f05bb331242dc3e3603983a61633e02818d2d0723f8c0519e`

```dockerfile
```

-	Layers:
	-	`sha256:cce27e898ff0ebb9bf564fd69c48c80d78943b1396e94c81770dbb243d430e65`  
		Last Modified: Tue, 17 Feb 2026 21:32:09 GMT  
		Size: 2.3 MB (2295947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:030d66698abf6f08f20821ad42613312a3e1bed1973a9dc56c6c4ee32a28a16c`  
		Last Modified: Tue, 17 Feb 2026 21:32:09 GMT  
		Size: 8.9 KB (8929 bytes)  
		MIME: application/vnd.in-toto+json
